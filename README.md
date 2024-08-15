<xml xmlns="https://developers.google.com/blockly/xml">
  <variables>
    <variable type="" id="gX!qt],R*YC4Q_Q1k.MJ">stake</variable>
    <variable type="" id="Bm]H;F5p^gxqx1h2G+Sn">lastTradeResult</variable>
  </variables>
  <block type="trade" id="^+RyZC9NJY1L*7HcX56v" x="12" y="12">
    <field name="TRADE_TYPE">CALL</field>
    <field name="DURATION">1</field>
    <field name="CONTRACT_TYPE">DIGITUNDER</field>
    <value name="DURATION_VALUE">
      <block type="math_number" id="bh%:lGh9Ao3Sx[aiJCMz">
        <field name="NUM">1</field>
      </block>
    </value>
    <value name="PAYOUT">
      <block type="math_number" id="x-cB+Y5K0DR=K#-nM=TF">
        <field name="NUM">10</field>
      </block>
    </value>
    <value name="BARRIER">
      <block type="math_number" id="yD_-d|A-XtX.}c~Z6Atp">
        <field name="NUM">9</field>
      </block>
    </value>
    <value name="AMOUNT">
      <block type="variables_get" id="nY=;7U,,t8oz2[09FzH=">
        <field name="VAR" id="gX!qt],R*YC4Q_Q1k.MJ">stake</field>
      </block>
    </value>
  </block>
  <block type="on_finish" id="HSuRU2i6,+zJV@F1gD*b" x="12" y="112">
    <value name="BOT_FINISHED">
      <block type="variables_set" id="Y?@@Ba#LaBIlp,3dC[pe">
        <field name="VAR" id="Bm]H;F5p^gxqx1h2G+Sn">lastTradeResult</field>
        <value name="VALUE">
          <block type="check_result" id="6Yh^:4;Vp%[CxRgyb1%S"></block>
        </value>
      </block>
    </value>
    <next>
      <block type="controls_if" id="J59-RW0^QmJZrxl{q,Z2">
        <value name="IF0">
          <block type="logic_compare" id="84pFvH_[HmrN_0m.d1Pd">
            <field name="OP">EQ</field>
            <value name="A">
              <block type="variables_get" id=")a9h]Z;4Ug5J:L^kgRH|">
                <field name="VAR" id="Bm]H;F5p^gxqx1h2G+Sn">lastTradeResult</field>
              </block>
            </value>
            <value name="B">
              <block type="text" id="G]aCLcG:-/FyJqP:?exk">
                <field name="TEXT">loss</field>
              </block>
            </value>
          </block>
        </value>
        <statement name="DO0">
          <block type="controls_if" id="WQtUMgpW^kM5H.Z5XODl">
            <value name="IF0">
              <block type="logic_boolean" id="pzC,{_J{?SJ!.]!u=~UV">
                <field name="BOOL">TRUE</field>
              </block>
            </value>
            <statement name="DO0">
              <block type="trade" id="S9gfMAIXyQq^%kzT9Tw-">
                <field name="TRADE_TYPE">CALL</field>
                <field name="DURATION">1</field>
                <field name="CONTRACT_TYPE">DIGITUNDER</field>
                <value name="DURATION_VALUE">
                  <block type="math_number" id="5*Ztck[m$9P_:o.6U,ls">
                    <field name="NUM">1</field>
                  </block>
                </value>
                <value name="PAYOUT">
                  <block type="math_number" id="p]GZ}6a_9jI,5Mgm=w*4">
                    <field name="NUM">10</field>
                  </block>
                </value>
                <value name="BARRIER">
                  <block type="math_number" id="5sHPHVJ}0`^:hhyL%.9y">
                    <field name="NUM">7</field>
                  </block>
                </value>
                <value name="AMOUNT">
                  <block type="math_arithmetic" id="41yx4HLQY0R?I@ajA]eA">
                    <field name="OP">MULTIPLY</field>
                    <value name="A">
                      <block type="variables_get" id="m9.NB{F[EDKc{yOd4EoI">
                        <field name="VAR" id="gX!qt],R*YC4Q_Q1k.MJ">stake</field>
                      </block>
                    </value>
                    <value name="B">
                      <block type="math_number" id="^}+ZOoR+qQDTiyZ0-Q*~">
                        <field name="NUM">3</field>
                      </block>
                    </value>
                  </block>
                </value>
              </block>
            </statement>
          </block>
        </statement>
      </block>
    </next>
  </block>
  <block type="variables_set" id="Z3%Q-1kP9hsfCboIo2Dt" x="12" y="312">
    <field name="VAR" id="gX!qt],R*YC4Q_Q1k.MJ">stake</field>
    <value name="VALUE">
      <block type="math_number" id="NStxS69]=;OUgE*26QfS">
        <field name="NUM">1</field>
      </block>
    </value>
  </block>
</xml>
