title: mybatis avg not work
date: 2016-06-28 09:37:47
categories: 【Mybatis】
tags: [Mybatis, SQL]
---
## {{ title }} ##

---

今天在配置mybatis的时候，发现虽然返回集的大小是有的，但是里面的数值都是null，我的代码是这样的：

```
	<select id="calAVGHealthScoreSet" resultMap="HealthScoreMap" parameterType="edu.sjtu.db.model.raw_data.OrderProperty">
		select AVG(HEALTHSCORE),AVG(QUALITYFACTOR),AVG(COLLABORATIONFACTOR),AVG(MEMBERFACTOR),AVG(SCHEDULEFACTOR)
	    from jf_order_property
	    <trim prefix="group by" suffix=";" suffixOverrides="," >
	      <if test="worktype != null" >
	        WORKTYPE,
	      </if>
	      <if test="domain != null" >
	        DOMAIN,
	      </if>
	      <if test="price != null" >
	        PRICE,
	      </if>
	      <if test="duration != null" >
	        DURATION,
	      </if>
	      <if test="memberYear != null" >
	        MEMBER_YEAR
	      </if>
	    </trim>
	</select>
```

resultMap是我定义的，由5个float变量组成，我这个sql是为了获取根据分组后的平均值。

需要为HealthScoreMap指明映射的对象