---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppSetting.md
ms.openlocfilehash: abfa704b042b0a8cd25b8682e3b93306b5ca6277
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136862"
---
# <span data-ttu-id="4102e-101">Remove-AzFunctionAppSetting</span><span class="sxs-lookup"><span data-stu-id="4102e-101">Remove-AzFunctionAppSetting</span></span>

## <span data-ttu-id="4102e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4102e-102">SYNOPSIS</span></span>
<span data-ttu-id="4102e-103">從函數 app 移除 app 設定。</span><span class="sxs-lookup"><span data-stu-id="4102e-103">Removes app settings from a function app.</span></span>

## <span data-ttu-id="4102e-104">句法</span><span class="sxs-lookup"><span data-stu-id="4102e-104">SYNTAX</span></span>

### <span data-ttu-id="4102e-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="4102e-105">ByName (Default)</span></span>
```
Remove-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> -AppSettingName <String[]>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4102e-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="4102e-106">ByObjectInput</span></span>
```
Remove-AzFunctionAppSetting -AppSettingName <String[]> -InputObject <ISite> [-Force]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4102e-107">說明</span><span class="sxs-lookup"><span data-stu-id="4102e-107">DESCRIPTION</span></span>
<span data-ttu-id="4102e-108">從函數 app 移除 app 設定。</span><span class="sxs-lookup"><span data-stu-id="4102e-108">Removes app settings from a function app.</span></span>

## <span data-ttu-id="4102e-109">示例</span><span class="sxs-lookup"><span data-stu-id="4102e-109">EXAMPLES</span></span>

### <span data-ttu-id="4102e-110">範例1：移除函數 app 中的 app 設定。</span><span class="sxs-lookup"><span data-stu-id="4102e-110">Example 1: Remove app settings in a function app.</span></span>
```powershell
PS C:\> Remove-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName -AppSettingName "MyAppSetting1", "MyAppSetting2"
```

<span data-ttu-id="4102e-111">這個命令會移除函數 app 中的 app 設定。</span><span class="sxs-lookup"><span data-stu-id="4102e-111">This command removes app settings in a function app.</span></span>

## <span data-ttu-id="4102e-112">參數</span><span class="sxs-lookup"><span data-stu-id="4102e-112">PARAMETERS</span></span>

### <span data-ttu-id="4102e-113">-AppSettingName</span><span class="sxs-lookup"><span data-stu-id="4102e-113">-AppSettingName</span></span>
<span data-ttu-id="4102e-114">要從函數 app 移除的函數 app 設定清單。</span><span class="sxs-lookup"><span data-stu-id="4102e-114">List of function app settings to be removed from the function app.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4102e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4102e-115">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4102e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4102e-116">-Force</span></span>
<span data-ttu-id="4102e-117">強制 Cmdlet 移除函式應用程式設定，而不提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4102e-117">Forces the cmdlet to remove function app setting without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4102e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4102e-118">-InputObject</span></span>
<span data-ttu-id="4102e-119">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4102e-119">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4102e-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="4102e-120">-Name</span></span>
<span data-ttu-id="4102e-121">函數應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="4102e-121">Name of the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4102e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4102e-122">-ResourceGroupName</span></span>
<span data-ttu-id="4102e-123">資源所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4102e-123">Name of the resource group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4102e-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4102e-124">-SubscriptionId</span></span>
<span data-ttu-id="4102e-125">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="4102e-125">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4102e-126">-確認</span><span class="sxs-lookup"><span data-stu-id="4102e-126">-Confirm</span></span>
<span data-ttu-id="4102e-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4102e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4102e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4102e-128">-WhatIf</span></span>
<span data-ttu-id="4102e-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4102e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4102e-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4102e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4102e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4102e-131">CommonParameters</span></span>
<span data-ttu-id="4102e-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4102e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4102e-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4102e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4102e-134">輸入</span><span class="sxs-lookup"><span data-stu-id="4102e-134">INPUTS</span></span>

### <span data-ttu-id="4102e-135">ISite 中的 Api20190801，然後再</span><span class="sxs-lookup"><span data-stu-id="4102e-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="4102e-136">輸出</span><span class="sxs-lookup"><span data-stu-id="4102e-136">OUTPUTS</span></span>

### <span data-ttu-id="4102e-137">IStringDictionary 中的 Api20190801，然後再</span><span class="sxs-lookup"><span data-stu-id="4102e-137">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span></span>

## <span data-ttu-id="4102e-138">筆記</span><span class="sxs-lookup"><span data-stu-id="4102e-138">NOTES</span></span>

<span data-ttu-id="4102e-139">別名</span><span class="sxs-lookup"><span data-stu-id="4102e-139">ALIASES</span></span>

<span data-ttu-id="4102e-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="4102e-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4102e-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="4102e-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4102e-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="4102e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4102e-143">INPUTOBJECT <ISite> ：</span><span class="sxs-lookup"><span data-stu-id="4102e-143">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="4102e-144">`Location <String>`：資源位置。</span><span class="sxs-lookup"><span data-stu-id="4102e-144">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="4102e-145">`CloningInfoSourceWebAppId <String>`：源 app 的 ARM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4102e-145">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="4102e-146">App 資源識別碼的形式是生產槽的表單/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}，而其他槽的/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} 則是。</span><span class="sxs-lookup"><span data-stu-id="4102e-146">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="4102e-147">`[Kind <String>]`：資源類型。</span><span class="sxs-lookup"><span data-stu-id="4102e-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="4102e-148">`[Tag <IResourceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="4102e-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="4102e-149">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="4102e-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="4102e-150">`[ClientAffinityEnabled <Boolean?>]`： <code>true</code> 若要啟用客戶關係 <code>false</code> ，請停止傳送會話相關性 cookie，該 cookie 會將同一個會話中的用戶端要求路由至同一個實例。</span><span class="sxs-lookup"><span data-stu-id="4102e-150">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="4102e-151">預設值為 <code>true</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-151">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="4102e-152">`[ClientCertEnabled <Boolean?>]`： <code>true</code> 若要啟用用戶端憑證驗證 (TLS 相互驗證) ; 否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-152">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="4102e-153">預設值為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-153">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="4102e-154">`[ClientCertExclusionPath <String>]`：用戶端憑證驗證以逗號分隔的排除路徑</span><span class="sxs-lookup"><span data-stu-id="4102e-154">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="4102e-155">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`：適用于克隆之 app 的應用程式設定覆寫。</span><span class="sxs-lookup"><span data-stu-id="4102e-155">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="4102e-156">如果已指定，這些設定會覆寫從源 app 克隆的設定。</span><span class="sxs-lookup"><span data-stu-id="4102e-156">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="4102e-157">否則，來源應用程式的應用程式設定會保留下來。</span><span class="sxs-lookup"><span data-stu-id="4102e-157">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="4102e-158">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="4102e-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="4102e-159">`[CloningInfoCloneCustomHostName <Boolean?>]`： <code>true</code> 若要從來源 app 克隆自訂主機名稱，否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-159">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="4102e-160">`[CloningInfoCloneSourceControl <Boolean?>]`： <code>true</code> 若要從來源應用程式克隆來源控制，否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-160">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="4102e-161">`[CloningInfoConfigureLoadBalancing <Boolean?>]`： <code>true</code> 為來源和目的地 app 設定負載平衡。</span><span class="sxs-lookup"><span data-stu-id="4102e-161">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="4102e-162">`[CloningInfoCorrelationId <String>]`：克隆作業的相關 ID。</span><span class="sxs-lookup"><span data-stu-id="4102e-162">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="4102e-163">這個識別碼將多個克隆作業結合在一起，以使用相同的快照。</span><span class="sxs-lookup"><span data-stu-id="4102e-163">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="4102e-164">`[CloningInfoHostingEnvironment <String>]`： App 服務環境。</span><span class="sxs-lookup"><span data-stu-id="4102e-164">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="4102e-165">`[CloningInfoOverwrite <Boolean?>]`： <code>true</code> 要覆寫目的地 app; 否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-165">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="4102e-166">`[CloningInfoSourceWebAppLocation <String>]`：來源應用程式的位置（例如：西美國或北歐）</span><span class="sxs-lookup"><span data-stu-id="4102e-166">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="4102e-167">`[CloningInfoTrafficManagerProfileId <String>]`：要使用之流量管理器設定檔的 ARM 資源識別碼（如果存在的話）。</span><span class="sxs-lookup"><span data-stu-id="4102e-167">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="4102e-168">流量管理員資源識別碼的形式為/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}。</span><span class="sxs-lookup"><span data-stu-id="4102e-168">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="4102e-169">`[CloningInfoTrafficManagerProfileName <String>]`：要建立之流量管理器設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="4102e-169">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="4102e-170">只有流量管理器設定檔尚不存在時，才需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="4102e-170">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="4102e-171">`[Config <ISiteConfig>]`：應用程式的配置。</span><span class="sxs-lookup"><span data-stu-id="4102e-171">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="4102e-172">`IsPushEnabled <Boolean>`：取得或設定指示是否已啟用推播端點的標誌。</span><span class="sxs-lookup"><span data-stu-id="4102e-172">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="4102e-173">`[ActionMinProcessExecutionTime <String>]`：在採取動作前必須執行的最短時間。</span><span class="sxs-lookup"><span data-stu-id="4102e-173">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="4102e-174">`[ActionType <AutoHealActionType?>]`：預先定義的要採取的動作。</span><span class="sxs-lookup"><span data-stu-id="4102e-174">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="4102e-175">`[AlwaysOn <Boolean?>]`： <code>true</code> 如果啟用 [永不開啟]，則為（否則，） <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-175">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="4102e-176">`[ApiDefinitionUrl <String>]`： API 定義的 URL。</span><span class="sxs-lookup"><span data-stu-id="4102e-176">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="4102e-177">`[ApiManagementConfigId <String>]`： APIM-Api 識別碼。</span><span class="sxs-lookup"><span data-stu-id="4102e-177">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="4102e-178">`[AppCommandLine <String>]`：啟動 App 命令列。</span><span class="sxs-lookup"><span data-stu-id="4102e-178">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="4102e-179">`[AppSetting <INameValuePair[]>]`：應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="4102e-179">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="4102e-180">`[Name <String>]`：配對名。</span><span class="sxs-lookup"><span data-stu-id="4102e-180">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="4102e-181">`[Value <String>]`： [配對] 值。</span><span class="sxs-lookup"><span data-stu-id="4102e-181">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="4102e-182">`[AutoHealEnabled <Boolean?>]`： <code>true</code> 如果已啟用自動修復，則為（否則，） <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-182">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="4102e-183">`[AutoSwapSlotName <String>]`：自動交換槽名稱。</span><span class="sxs-lookup"><span data-stu-id="4102e-183">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="4102e-184">`[ConnectionString <IConnStringInfo[]>]`：連接字串。</span><span class="sxs-lookup"><span data-stu-id="4102e-184">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="4102e-185">`[ConnectionString <String>]`：連接字串值。</span><span class="sxs-lookup"><span data-stu-id="4102e-185">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="4102e-186">`[Name <String>]`：連接字串的名稱。</span><span class="sxs-lookup"><span data-stu-id="4102e-186">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="4102e-187">`[Type <ConnectionStringType?>]`：資料庫的類型。</span><span class="sxs-lookup"><span data-stu-id="4102e-187">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="4102e-188">`[CorAllowedOrigin <String[]>]`：取得或設定允許進行交叉起源撥打電話的來源清單 (例如： http://example.com:12345) 。</span><span class="sxs-lookup"><span data-stu-id="4102e-188">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="4102e-189">使用 "\*" 全部允許。</span><span class="sxs-lookup"><span data-stu-id="4102e-189">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="4102e-190">`[CorSupportCredentials <Boolean?>]`：取得或設定是否允許含身分驗證的 CORS 要求。</span><span class="sxs-lookup"><span data-stu-id="4102e-190">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="4102e-191">如需詳細         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         資訊，請參閱。</span><span class="sxs-lookup"><span data-stu-id="4102e-191">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="4102e-192">`[CustomActionExe <String>]`：要執行的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="4102e-192">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="4102e-193">`[CustomActionParameter <String>]`：可執行檔的參數。</span><span class="sxs-lookup"><span data-stu-id="4102e-193">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="4102e-194">`[DefaultDocument <String[]>]`：預設檔。</span><span class="sxs-lookup"><span data-stu-id="4102e-194">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="4102e-195">`[DetailedErrorLoggingEnabled <Boolean?>]`： <code>true</code> 如果已啟用詳細的錯誤記錄，則為（否則，） <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-195">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="4102e-196">`[DocumentRoot <String>]`：檔根。</span><span class="sxs-lookup"><span data-stu-id="4102e-196">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="4102e-197">`[DynamicTagsJson <String>]`：取得或設定一個 JSON 字串，其中包含將從推入註冊端點中的使用者宣告評估的動態標記清單。</span><span class="sxs-lookup"><span data-stu-id="4102e-197">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="4102e-198">`[ExperimentRampUpRule <IRampUpRule[]>]`：提升式規則清單。</span><span class="sxs-lookup"><span data-stu-id="4102e-198">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="4102e-199">`[ActionHostName <String>]`：如果決定要將流量重新導向到的槽主機名稱。</span><span class="sxs-lookup"><span data-stu-id="4102e-199">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="4102e-200">例如.</span><span class="sxs-lookup"><span data-stu-id="4102e-200">E.g.</span></span> <span data-ttu-id="4102e-201">myapp-stage.azurewebsites.net。</span><span class="sxs-lookup"><span data-stu-id="4102e-201">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="4102e-202">`[ChangeDecisionCallbackUrl <String>]`：您可以在 TiPCallback 網站副檔名中提供自訂決策演算法，您可以指定此 URL。</span><span class="sxs-lookup"><span data-stu-id="4102e-202">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="4102e-203">請參閱架設與合約的 TiPCallback 網站延伸。</span><span class="sxs-lookup"><span data-stu-id="4102e-203">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="4102e-204"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="4102e-204">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="4102e-205">`[ChangeIntervalInMinute <Int32?>]`：指定要重新評估 ReroutePercentage 的間隔時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="4102e-205">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="4102e-206">`[ChangeStep <Double?>]`：在自動向上斜坡案例中，這是要新增/移除的步驟， <code>ReroutePercentage</code> 直到到達 \n <code>MinReroutePercentage</code> 或         <code>MaxReroutePercentage</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-206">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="4102e-207">在 .\NCustom 決策演算法中指定的每 N 分鐘數，都 <code>ChangeIntervalInMinutes</code> 可以在 TiPCallback 網站副檔名中提供，您可以在其中指定 URL <code>ChangeDecisionCallbackUrl</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-207">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="4102e-208">`[MaxReroutePercentage <Double?>]`：指定 ReroutePercentage 將持續的上限。</span><span class="sxs-lookup"><span data-stu-id="4102e-208">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="4102e-209">`[MinReroutePercentage <Double?>]`：指定 ReroutePercentage 將持續的較低邊界。</span><span class="sxs-lookup"><span data-stu-id="4102e-209">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="4102e-210">`[Name <String>]`：路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="4102e-210">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="4102e-211">建議的名稱是指向將在實驗中接收流量的槽。</span><span class="sxs-lookup"><span data-stu-id="4102e-211">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="4102e-212">`[ReroutePercentage <Double?>]`：將會重新導向之流量的百分比 <code>ActionHostName</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-212">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="4102e-213">`[FtpsState <FtpsState?>]`： FTP/FTPS 服務的狀態</span><span class="sxs-lookup"><span data-stu-id="4102e-213">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="4102e-214">`[HandlerMapping <IHandlerMapping[]>]`：處理常式對應。</span><span class="sxs-lookup"><span data-stu-id="4102e-214">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="4102e-215">`[Argument <String>]`：要傳送至腳本處理器的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="4102e-215">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="4102e-216">`[Extension <String>]`：具有此延伸的要求將會使用指定的 FastCGI 應用程式來處理。</span><span class="sxs-lookup"><span data-stu-id="4102e-216">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="4102e-217">`[ScriptProcessor <String>]`： FastCGI 應用程式的絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="4102e-217">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="4102e-218">`[HealthCheckPath <String>]`：健康情況檢查路徑</span><span class="sxs-lookup"><span data-stu-id="4102e-218">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="4102e-219">`[Http20Enabled <Boolean?>]`： Http20Enabled：將網站設定為允許用戶端經由 HTTP 2.0 連線</span><span class="sxs-lookup"><span data-stu-id="4102e-219">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="4102e-220">`[HttpLoggingEnabled <Boolean?>]`： <code>true</code> 如果已啟用 HTTP 記錄，則為，否則為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-220">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="4102e-221">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`：主要的 IP 安全性限制。</span><span class="sxs-lookup"><span data-stu-id="4102e-221">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="4102e-222">`[Action <String>]`：允許或拒絕此 IP 範圍的存取權。</span><span class="sxs-lookup"><span data-stu-id="4102e-222">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="4102e-223">`[Description <String>]`： IP 限制規則描述。</span><span class="sxs-lookup"><span data-stu-id="4102e-223">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="4102e-224">`[IPAddress <String>]`： [安全性限制] 適用的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="4102e-224">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="4102e-225">它可以是純 ipv4 位址的形式 (必要的 SubnetMask 屬性) 或 CIDR 符號（例如 ipv4/遮罩 (前導位相符）) 。</span><span class="sxs-lookup"><span data-stu-id="4102e-225">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="4102e-226">若是 CIDR，則不得指定 SubnetMask 屬性。</span><span class="sxs-lookup"><span data-stu-id="4102e-226">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="4102e-227">`[Name <String>]`： IP 限制規則名稱。</span><span class="sxs-lookup"><span data-stu-id="4102e-227">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="4102e-228">`[Priority <Int32?>]`： IP 限制規則的優先順序。</span><span class="sxs-lookup"><span data-stu-id="4102e-228">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="4102e-229">`[SubnetMask <String>]`：限制有效的 IP 位址範圍的子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="4102e-229">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="4102e-230">`[SubnetTrafficTag <Int32?>]`： (內部) 子網流量標記</span><span class="sxs-lookup"><span data-stu-id="4102e-230">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="4102e-231">`[Tag <IPFilterTag?>]`：定義此 IP 篩選將用於何種用途。</span><span class="sxs-lookup"><span data-stu-id="4102e-231">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="4102e-232">這是為了支援在 proxy 上進行 IP 篩選。</span><span class="sxs-lookup"><span data-stu-id="4102e-232">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="4102e-233">`[VnetSubnetResourceId <String>]`：虛擬網路資源識別碼</span><span class="sxs-lookup"><span data-stu-id="4102e-233">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="4102e-234">`[VnetTrafficTag <Int32?>]`： (內部) Vnet 流量標記</span><span class="sxs-lookup"><span data-stu-id="4102e-234">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="4102e-235">`[JavaContainer <String>]`： JAVA 容器。</span><span class="sxs-lookup"><span data-stu-id="4102e-235">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="4102e-236">`[JavaContainerVersion <String>]`： JAVA 容器版本。</span><span class="sxs-lookup"><span data-stu-id="4102e-236">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="4102e-237">`[JavaVersion <String>]`： JAVA 版本。</span><span class="sxs-lookup"><span data-stu-id="4102e-237">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="4102e-238">`[LimitMaxDiskSizeInMb <Int64?>]`：允許的磁片大小上限，以 MB 為單位。</span><span class="sxs-lookup"><span data-stu-id="4102e-238">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="4102e-239">`[LimitMaxMemoryInMb <Int64?>]`：允許的最大記憶體使用量（MB）。</span><span class="sxs-lookup"><span data-stu-id="4102e-239">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="4102e-240">`[LimitMaxPercentageCpu <Double?>]`：允許的 CPU 使用量上限百分比。</span><span class="sxs-lookup"><span data-stu-id="4102e-240">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="4102e-241">`[LinuxFxVersion <String>]`： Linux App 架構與版本</span><span class="sxs-lookup"><span data-stu-id="4102e-241">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="4102e-242">`[LoadBalancing <SiteLoadBalancing?>]`：網站負載平衡。</span><span class="sxs-lookup"><span data-stu-id="4102e-242">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="4102e-243">`[LocalMySqlEnabled <Boolean?>]`： <code>true</code> 若要啟用本機 MySQL，否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-243">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="4102e-244">`[LogsDirectorySizeLimit <Int32?>]`： HTTP 記錄目錄大小限制。</span><span class="sxs-lookup"><span data-stu-id="4102e-244">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="4102e-245">`[MachineKeyDecryption <String>]`：用於解密的演算法。</span><span class="sxs-lookup"><span data-stu-id="4102e-245">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="4102e-246">`[MachineKeyDecryptionKey <String>]`：解密金鑰。</span><span class="sxs-lookup"><span data-stu-id="4102e-246">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="4102e-247">`[MachineKeyValidation <String>]`： MachineKey 驗證。</span><span class="sxs-lookup"><span data-stu-id="4102e-247">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="4102e-248">`[MachineKeyValidationKey <String>]`：驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="4102e-248">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="4102e-249">`[ManagedPipelineMode <ManagedPipelineMode?>]`：受管理的管線模式。</span><span class="sxs-lookup"><span data-stu-id="4102e-249">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="4102e-250">`[ManagedServiceIdentityId <Int32?>]`：受管理的服務身分識別識別碼</span><span class="sxs-lookup"><span data-stu-id="4102e-250">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="4102e-251">`[MinTlsVersion <SupportedTlsVersions?>]`： MinTlsVersion：設定 SSL 要求所需的最小 TLS 版本</span><span class="sxs-lookup"><span data-stu-id="4102e-251">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="4102e-252">`[NetFrameworkVersion <String>]`： .NET Framework 版本。</span><span class="sxs-lookup"><span data-stu-id="4102e-252">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="4102e-253">`[NodeVersion <String>]`： Node.js 版本。</span><span class="sxs-lookup"><span data-stu-id="4102e-253">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="4102e-254">`[NumberOfWorker <Int32?>]`：工人的人數。</span><span class="sxs-lookup"><span data-stu-id="4102e-254">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="4102e-255">`[PhpVersion <String>]`： PHP 版本。</span><span class="sxs-lookup"><span data-stu-id="4102e-255">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="4102e-256">`[PowerShellVersion <String>]`： PowerShell 版本。</span><span class="sxs-lookup"><span data-stu-id="4102e-256">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="4102e-257">`[PreWarmedInstanceCount <Int32?>]`： PreWarmed 實例數。</span><span class="sxs-lookup"><span data-stu-id="4102e-257">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="4102e-258">此設定僅適用于消耗量與彈性方案</span><span class="sxs-lookup"><span data-stu-id="4102e-258">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="4102e-259">`[PublishingUsername <String>]`：發佈使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="4102e-259">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="4102e-260">`[PushKind <String>]`：資源類型。</span><span class="sxs-lookup"><span data-stu-id="4102e-260">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="4102e-261">`[PythonVersion <String>]`： Python 版本。</span><span class="sxs-lookup"><span data-stu-id="4102e-261">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="4102e-262">`[RemoteDebuggingEnabled <Boolean?>]`： <code>true</code> 如果已啟用遠端偵錯，則為，否則為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-262">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="4102e-263">`[RemoteDebuggingVersion <String>]`：遠端偵錯版本。</span><span class="sxs-lookup"><span data-stu-id="4102e-263">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="4102e-264">`[RequestCount <Int32?>]`： [要求計數]。</span><span class="sxs-lookup"><span data-stu-id="4102e-264">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="4102e-265">`[RequestTimeInterval <String>]`：時間間隔。</span><span class="sxs-lookup"><span data-stu-id="4102e-265">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="4102e-266">`[RequestTracingEnabled <Boolean?>]`： <code>true</code> 如果已啟用要求追蹤，則為（否則，） <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-266">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="4102e-267">`[RequestTracingExpirationTime <DateTime?>]`：要求追蹤到期時間。</span><span class="sxs-lookup"><span data-stu-id="4102e-267">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="4102e-268">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`：適用于 scm 的 IP 安全性限制。</span><span class="sxs-lookup"><span data-stu-id="4102e-268">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="4102e-269">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`：適用于 scm 的 IP 安全性限制使用 main。</span><span class="sxs-lookup"><span data-stu-id="4102e-269">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="4102e-270">`[ScmType <ScmType?>]`： SCM 類型。</span><span class="sxs-lookup"><span data-stu-id="4102e-270">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="4102e-271">`[SlowRequestCount <Int32?>]`： [要求計數]。</span><span class="sxs-lookup"><span data-stu-id="4102e-271">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="4102e-272">`[SlowRequestTimeInterval <String>]`：時間間隔。</span><span class="sxs-lookup"><span data-stu-id="4102e-272">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="4102e-273">`[SlowRequestTimeTaken <String>]`：拍攝的時間。</span><span class="sxs-lookup"><span data-stu-id="4102e-273">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="4102e-274">`[TagWhitelistJson <String>]`：取得或設定一個 JSON 字串，其中包含由推入註冊端點所使用的白板標記清單。</span><span class="sxs-lookup"><span data-stu-id="4102e-274">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="4102e-275">`[TagsRequiringAuth <String>]`：取得或設定一個 JSON 字串，其中包含需要使用者驗證才能用於推入註冊端點的標記清單。</span><span class="sxs-lookup"><span data-stu-id="4102e-275">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="4102e-276">標記可以由字母數位字元及下列專案所組成：「_ '、' @ '、' # '、'. '、'： '、'-」。</span><span class="sxs-lookup"><span data-stu-id="4102e-276">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="4102e-277">驗證應該在 PushRequestHandler 進行。</span><span class="sxs-lookup"><span data-stu-id="4102e-277">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="4102e-278">`[TracingOption <String>]`：追蹤選項。</span><span class="sxs-lookup"><span data-stu-id="4102e-278">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="4102e-279">`[TriggerPrivateBytesInKb <Int32?>]`：以私人位元組為基礎的規則。</span><span class="sxs-lookup"><span data-stu-id="4102e-279">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="4102e-280">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`：以狀態碼為基礎的規則。</span><span class="sxs-lookup"><span data-stu-id="4102e-280">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="4102e-281">`[Count <Int32?>]`： [要求計數]。</span><span class="sxs-lookup"><span data-stu-id="4102e-281">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="4102e-282">`[Status <Int32?>]`： HTTP 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="4102e-282">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="4102e-283">`[SubStatus <Int32?>]`：要求子狀態。</span><span class="sxs-lookup"><span data-stu-id="4102e-283">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="4102e-284">`[TimeInterval <String>]`：時間間隔。</span><span class="sxs-lookup"><span data-stu-id="4102e-284">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="4102e-285">`[Win32Status <Int32?>]`： Win32 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4102e-285">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="4102e-286">`[Use32BitWorkerProcess <Boolean?>]`： <code>true</code> 若要使用32位的輔助進程，請按相反的方式 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-286">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="4102e-287">`[VirtualApplication <IVirtualApplication[]>]`：虛擬應用程式。</span><span class="sxs-lookup"><span data-stu-id="4102e-287">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="4102e-288">`[PhysicalPath <String>]`：實體路徑。</span><span class="sxs-lookup"><span data-stu-id="4102e-288">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="4102e-289">`[PreloadEnabled <Boolean?>]`： <code>true</code> 如果已啟用預載入，則為，否則為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-289">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="4102e-290">`[VirtualDirectory <IVirtualDirectory[]>]`：虛擬應用程式的虛擬目錄。</span><span class="sxs-lookup"><span data-stu-id="4102e-290">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="4102e-291">`[PhysicalPath <String>]`：實體路徑。</span><span class="sxs-lookup"><span data-stu-id="4102e-291">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="4102e-292">`[VirtualPath <String>]`：虛擬應用程式的路徑。</span><span class="sxs-lookup"><span data-stu-id="4102e-292">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="4102e-293">`[VirtualPath <String>]`：虛擬路徑。</span><span class="sxs-lookup"><span data-stu-id="4102e-293">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="4102e-294">`[VnetName <String>]`：虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="4102e-294">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="4102e-295">`[WebSocketsEnabled <Boolean?>]`： <code>true</code> 如果已啟用 WebSocket，則為，否則為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-295">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="4102e-296">`[WindowsFxVersion <String>]`： Xenon 應用程式架構與版本</span><span class="sxs-lookup"><span data-stu-id="4102e-296">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="4102e-297">`[XManagedServiceIdentityId <Int32?>]`：顯式管理的服務身分識別識別碼</span><span class="sxs-lookup"><span data-stu-id="4102e-297">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="4102e-298">`[ContainerSize <Int32?>]`：函數容器的大小。</span><span class="sxs-lookup"><span data-stu-id="4102e-298">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="4102e-299">`[DailyMemoryTimeQuota <Int32?>]`： (僅適用于動態 app 的 [允許的每日記憶體時間配額限制]) 。</span><span class="sxs-lookup"><span data-stu-id="4102e-299">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="4102e-300">`[Enabled <Boolean?>]`： <code>true</code> 如果已啟用應用程式，否則為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-300">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="4102e-301">將此值設定為 false 會停用 app (將 app 離線) 。</span><span class="sxs-lookup"><span data-stu-id="4102e-301">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="4102e-302">`[HostNameSslState <IHostNameSslState[]>]`：主機名稱 SSL 狀態是用來管理 app 主機名稱的 SSL 系結。</span><span class="sxs-lookup"><span data-stu-id="4102e-302">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="4102e-303">`[HostType <HostType?>]`：表示主機名稱是標準版還是知識庫主機名稱。</span><span class="sxs-lookup"><span data-stu-id="4102e-303">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="4102e-304">`[Name <String>]`主機.</span><span class="sxs-lookup"><span data-stu-id="4102e-304">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="4102e-305">`[SslState <SslState?>]`： SSL 類型。</span><span class="sxs-lookup"><span data-stu-id="4102e-305">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="4102e-306">`[Thumbprint <String>]`： SSL 憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="4102e-306">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="4102e-307">`[ToUpdate <Boolean?>]`：設定為 <code>true</code> 以更新現有的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="4102e-307">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="4102e-308">`[VirtualIP <String>]`：如果啟用 IP SSL，則會指派給主機名稱的虛擬 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="4102e-308">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="4102e-309">`[HostNamesDisabled <Boolean?>]`： <code>true</code> 若要停用應用程式的公用主機名稱，否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-309">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="4102e-310">如果 <code>true</code> 是，只能透過 API 管理程式存取 app。</span><span class="sxs-lookup"><span data-stu-id="4102e-310">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="4102e-311">`[HostingEnvironmentProfileId <String>]`：應用程式服務環境的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4102e-311">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="4102e-312">`[HttpsOnly <Boolean?>]`： HttpsOnly：將網站配置為只接受 HTTPs 要求。</span><span class="sxs-lookup"><span data-stu-id="4102e-312">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="4102e-313">Http 要求的重新導向問題</span><span class="sxs-lookup"><span data-stu-id="4102e-313">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="4102e-314">`[HyperV <Boolean?>]`： Hyper-v 沙箱。</span><span class="sxs-lookup"><span data-stu-id="4102e-314">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="4102e-315">`[IdentityType <ManagedServiceIdentityType?>]`：受管理的服務身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="4102e-315">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="4102e-316">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`：指派與資源相關聯之身分識別的使用者清單。</span><span class="sxs-lookup"><span data-stu-id="4102e-316">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="4102e-317">使用者身分識別字典金鑰參照會是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="4102e-317">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="4102e-318">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="4102e-318">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="4102e-319">`[IsXenon <Boolean?>]`：已過時： Hyper-v 沙箱。</span><span class="sxs-lookup"><span data-stu-id="4102e-319">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="4102e-320">`[RedundancyMode <RedundancyMode?>]`：網站冗余模式</span><span class="sxs-lookup"><span data-stu-id="4102e-320">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="4102e-321">`[Reserved <Boolean?>]`： <code>true</code> 如果保留，則為，否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-321">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="4102e-322">`[ScmSiteAlsoStopped <Boolean?>]`： <code>true</code> 若要在應用程式停止時停止 SCM (KUDU) 網站，請按相反步驟操作 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-322">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="4102e-323">預設值為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="4102e-323">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="4102e-324">`[ServerFarmId <String>]`：相關應用程式服務方案的資源識別碼，格式為： "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}"。</span><span class="sxs-lookup"><span data-stu-id="4102e-324">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="4102e-325">相關連結</span><span class="sxs-lookup"><span data-stu-id="4102e-325">RELATED LINKS</span></span>

