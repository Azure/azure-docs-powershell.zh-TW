---
外部說明檔案： Microsoft.Azure.Commands.FrontDoor.dll-Help.xml 的模組名稱： AzureRM。 FrontDoor online 版本：對應的 URL 應如下所示： https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor schema： 2.0.0 content_git_url： https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url： https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md
---

# <a name="new-azurermfrontdoor"></a>New-AzureRmFrontDoor

## <a name="synopsis"></a>摘要
建立新的 Azure 前門負載平衡器

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <a name="syntax"></a>句法

```
New-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <a name="description"></a>說明
**新的-AzureRmFrontDoor** Cmdlet 會在指定資源群組中的 [目前訂閱] 下建立新的 Azure 前門負載平衡器。

## <a name="examples"></a>示例

### <a name="example-1-create-a-front-door-based-on-given-parameters"></a>範例1：根據指定的參數建立前門。
```powershell
PS C:\> New-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

根據指定的參數建立一個前門。

## <a name="parameters"></a>參數

### <a name="-backendpool"></a>-BackendPool
Backendpools 可供路由規則使用。

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-defaultprofile"></a>-DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-enabledstate"></a>-EnabledState
前蓋負載平衡器的 EnabledState。
已啟用預設值

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-frontendendpoint"></a>-FrontendEndpoint
可供路由規則使用的前端端點。

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-healthprobesetting"></a>-HealthProbeSetting
與此前門實例相關聯的健康情況探測器設定。

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-loadbalancingsetting"></a>-LoadBalancingSetting
與此前門實例相關聯的負載平衡設定。

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-name"></a>-名稱
前門名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-resourcegroupname"></a>-ResourceGroupName
在其中建立前蓋的資源群組名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-routingrule"></a>-RoutingRule
與此 FrontDoor 相關聯的路由規則

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-tag"></a>-Tag
標記與 FrontDoor 相關聯。

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-confirm"></a>-確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-whatif"></a>-WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="commonparameters"></a>CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## <a name="inputs"></a>輸入

### <a name="systemstring"></a>System.object

## <a name="outputs"></a>輸出

### <a name="microsoftazurecommandsfrontdoormodelspsfrontdoor"></a>PSFrontDoor 中的 FrontDoor。

## <a name="notes"></a>筆記

## <a name="related-links"></a>相關連結

[AzureRmFrontDoor](./Get-AzureRmFrontDoor.md) 
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
[移除-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md) 
[新-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
[新-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
[新-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
[新-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
[新-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)
