---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppSetting.md
ms.openlocfilehash: 4255940b9cf17420fe0b522d81c6a974e9cf9324
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278123"
---
# <span data-ttu-id="858c6-101">Update-AzFunctionAppSetting</span><span class="sxs-lookup"><span data-stu-id="858c6-101">Update-AzFunctionAppSetting</span></span>

## <span data-ttu-id="858c6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="858c6-102">SYNOPSIS</span></span>
<span data-ttu-id="858c6-103">在函數 app 中新增或更新應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="858c6-103">Adds or updates app settings in a function app.</span></span>

## <span data-ttu-id="858c6-104">句法</span><span class="sxs-lookup"><span data-stu-id="858c6-104">SYNTAX</span></span>

### <span data-ttu-id="858c6-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="858c6-105">ByName (Default)</span></span>
```
Update-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> -AppSetting <Hashtable>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="858c6-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="858c6-106">ByObjectInput</span></span>
```
Update-AzFunctionAppSetting -AppSetting <Hashtable> -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="858c6-107">說明</span><span class="sxs-lookup"><span data-stu-id="858c6-107">DESCRIPTION</span></span>
<span data-ttu-id="858c6-108">在函數 app 中新增或更新應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="858c6-108">Adds or updates app settings in a function app.</span></span>

## <span data-ttu-id="858c6-109">示例</span><span class="sxs-lookup"><span data-stu-id="858c6-109">EXAMPLES</span></span>

### <span data-ttu-id="858c6-110">範例1：在函數應用程式中新增新的應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="858c6-110">Example 1: Add a new app setting in a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName -AppSetting @{"Name1" = "Value1"}
```

<span data-ttu-id="858c6-111">這個命令會在函數 app 中新增一個新的應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="858c6-111">This command adds a new app setting in a function app.</span></span>

## <span data-ttu-id="858c6-112">參數</span><span class="sxs-lookup"><span data-stu-id="858c6-112">PARAMETERS</span></span>

### <span data-ttu-id="858c6-113">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="858c6-113">-AppSetting</span></span>
<span data-ttu-id="858c6-114">含鍵和值的 Hashtable 描述在函數應用程式中新增或更新的應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="858c6-114">Hashtable with keys and values describe the app settings to be added or updated in the function app.</span></span>
<span data-ttu-id="858c6-115">例如： @ {"myappsetting" = "123"}</span><span class="sxs-lookup"><span data-stu-id="858c6-115">For example: @{"myappsetting"="123"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="858c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="858c6-116">-DefaultProfile</span></span>


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

### <span data-ttu-id="858c6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="858c6-117">-Force</span></span>
<span data-ttu-id="858c6-118">強制 Cmdlet 更新函式應用程式設定，而不提示您確認。</span><span class="sxs-lookup"><span data-stu-id="858c6-118">Forces the cmdlet to update function app setting without prompting for confirmation.</span></span>

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

### <span data-ttu-id="858c6-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="858c6-119">-InputObject</span></span>
<span data-ttu-id="858c6-120">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="858c6-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="858c6-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="858c6-121">-Name</span></span>
<span data-ttu-id="858c6-122">函數應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="858c6-122">Name of the function app.</span></span>

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

### <span data-ttu-id="858c6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="858c6-123">-ResourceGroupName</span></span>
<span data-ttu-id="858c6-124">資源所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="858c6-124">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="858c6-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="858c6-125">-SubscriptionId</span></span>
<span data-ttu-id="858c6-126">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="858c6-126">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="858c6-127">-確認</span><span class="sxs-lookup"><span data-stu-id="858c6-127">-Confirm</span></span>
<span data-ttu-id="858c6-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="858c6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="858c6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="858c6-129">-WhatIf</span></span>
<span data-ttu-id="858c6-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="858c6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="858c6-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="858c6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="858c6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="858c6-132">CommonParameters</span></span>
<span data-ttu-id="858c6-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="858c6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="858c6-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="858c6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="858c6-135">輸入</span><span class="sxs-lookup"><span data-stu-id="858c6-135">INPUTS</span></span>

### <span data-ttu-id="858c6-136">ISite 中的 Api20190801，然後再</span><span class="sxs-lookup"><span data-stu-id="858c6-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="858c6-137">輸出</span><span class="sxs-lookup"><span data-stu-id="858c6-137">OUTPUTS</span></span>

### <span data-ttu-id="858c6-138">IStringDictionary 中的 Api20190801，然後再</span><span class="sxs-lookup"><span data-stu-id="858c6-138">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span></span>

## <span data-ttu-id="858c6-139">筆記</span><span class="sxs-lookup"><span data-stu-id="858c6-139">NOTES</span></span>

<span data-ttu-id="858c6-140">別名</span><span class="sxs-lookup"><span data-stu-id="858c6-140">ALIASES</span></span>

<span data-ttu-id="858c6-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="858c6-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="858c6-142">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="858c6-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="858c6-143">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="858c6-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="858c6-144">INPUTOBJECT <ISite> ：</span><span class="sxs-lookup"><span data-stu-id="858c6-144">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="858c6-145">`Location <String>`：資源位置。</span><span class="sxs-lookup"><span data-stu-id="858c6-145">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="858c6-146">`CloningInfoSourceWebAppId <String>`：源 app 的 ARM 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="858c6-146">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="858c6-147">App 資源識別碼的形式是生產槽的表單/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}，而其他槽的/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} 則是。</span><span class="sxs-lookup"><span data-stu-id="858c6-147">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="858c6-148">`[Kind <String>]`：資源類型。</span><span class="sxs-lookup"><span data-stu-id="858c6-148">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="858c6-149">`[Tag <IResourceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="858c6-149">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="858c6-150">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="858c6-150">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="858c6-151">`[ClientAffinityEnabled <Boolean?>]`： <code>true</code> 若要啟用客戶關係 <code>false</code> ，請停止傳送會話相關性 cookie，該 cookie 會將同一個會話中的用戶端要求路由至同一個實例。</span><span class="sxs-lookup"><span data-stu-id="858c6-151">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="858c6-152">預設值為 <code>true</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-152">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="858c6-153">`[ClientCertEnabled <Boolean?>]`： <code>true</code> 若要啟用用戶端憑證驗證 (TLS 相互驗證) ; 否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-153">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="858c6-154">預設值為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-154">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="858c6-155">`[ClientCertExclusionPath <String>]`：用戶端憑證驗證以逗號分隔的排除路徑</span><span class="sxs-lookup"><span data-stu-id="858c6-155">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="858c6-156">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`：適用于克隆之 app 的應用程式設定覆寫。</span><span class="sxs-lookup"><span data-stu-id="858c6-156">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="858c6-157">如果已指定，這些設定會覆寫從源 app 克隆的設定。</span><span class="sxs-lookup"><span data-stu-id="858c6-157">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="858c6-158">否則，來源應用程式的應用程式設定會保留下來。</span><span class="sxs-lookup"><span data-stu-id="858c6-158">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="858c6-159">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="858c6-159">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="858c6-160">`[CloningInfoCloneCustomHostName <Boolean?>]`： <code>true</code> 若要從來源 app 克隆自訂主機名稱，否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-160">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="858c6-161">`[CloningInfoCloneSourceControl <Boolean?>]`： <code>true</code> 若要從來源應用程式克隆來源控制，否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-161">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="858c6-162">`[CloningInfoConfigureLoadBalancing <Boolean?>]`： <code>true</code> 為來源和目的地 app 設定負載平衡。</span><span class="sxs-lookup"><span data-stu-id="858c6-162">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="858c6-163">`[CloningInfoCorrelationId <String>]`：克隆作業的相關 ID。</span><span class="sxs-lookup"><span data-stu-id="858c6-163">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="858c6-164">這個識別碼將多個克隆作業結合在一起，以使用相同的快照。</span><span class="sxs-lookup"><span data-stu-id="858c6-164">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="858c6-165">`[CloningInfoHostingEnvironment <String>]`： App 服務環境。</span><span class="sxs-lookup"><span data-stu-id="858c6-165">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="858c6-166">`[CloningInfoOverwrite <Boolean?>]`： <code>true</code> 要覆寫目的地 app; 否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-166">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="858c6-167">`[CloningInfoSourceWebAppLocation <String>]`：來源應用程式的位置（例如：西美國或北歐）</span><span class="sxs-lookup"><span data-stu-id="858c6-167">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="858c6-168">`[CloningInfoTrafficManagerProfileId <String>]`：要使用之流量管理器設定檔的 ARM 資源識別碼（如果存在的話）。</span><span class="sxs-lookup"><span data-stu-id="858c6-168">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="858c6-169">流量管理員資源識別碼的形式為/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}。</span><span class="sxs-lookup"><span data-stu-id="858c6-169">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="858c6-170">`[CloningInfoTrafficManagerProfileName <String>]`：要建立之流量管理器設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="858c6-170">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="858c6-171">只有流量管理器設定檔尚不存在時，才需要這麼做。</span><span class="sxs-lookup"><span data-stu-id="858c6-171">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="858c6-172">`[Config <ISiteConfig>]`：應用程式的配置。</span><span class="sxs-lookup"><span data-stu-id="858c6-172">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="858c6-173">`IsPushEnabled <Boolean>`：取得或設定指示是否已啟用推播端點的標誌。</span><span class="sxs-lookup"><span data-stu-id="858c6-173">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="858c6-174">`[ActionMinProcessExecutionTime <String>]`：在採取動作前必須執行的最短時間。</span><span class="sxs-lookup"><span data-stu-id="858c6-174">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="858c6-175">`[ActionType <AutoHealActionType?>]`：預先定義的要採取的動作。</span><span class="sxs-lookup"><span data-stu-id="858c6-175">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="858c6-176">`[AlwaysOn <Boolean?>]`： <code>true</code> 如果啟用 [永不開啟]，則為（否則，） <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-176">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="858c6-177">`[ApiDefinitionUrl <String>]`： API 定義的 URL。</span><span class="sxs-lookup"><span data-stu-id="858c6-177">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="858c6-178">`[ApiManagementConfigId <String>]`： APIM-Api 識別碼。</span><span class="sxs-lookup"><span data-stu-id="858c6-178">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="858c6-179">`[AppCommandLine <String>]`：啟動 App 命令列。</span><span class="sxs-lookup"><span data-stu-id="858c6-179">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="858c6-180">`[AppSetting <INameValuePair[]>]`：應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="858c6-180">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="858c6-181">`[Name <String>]`：配對名。</span><span class="sxs-lookup"><span data-stu-id="858c6-181">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="858c6-182">`[Value <String>]`： [配對] 值。</span><span class="sxs-lookup"><span data-stu-id="858c6-182">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="858c6-183">`[AutoHealEnabled <Boolean?>]`： <code>true</code> 如果已啟用自動修復，則為（否則，） <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-183">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="858c6-184">`[AutoSwapSlotName <String>]`：自動交換槽名稱。</span><span class="sxs-lookup"><span data-stu-id="858c6-184">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="858c6-185">`[ConnectionString <IConnStringInfo[]>]`：連接字串。</span><span class="sxs-lookup"><span data-stu-id="858c6-185">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="858c6-186">`[ConnectionString <String>]`：連接字串值。</span><span class="sxs-lookup"><span data-stu-id="858c6-186">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="858c6-187">`[Name <String>]`：連接字串的名稱。</span><span class="sxs-lookup"><span data-stu-id="858c6-187">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="858c6-188">`[Type <ConnectionStringType?>]`：資料庫的類型。</span><span class="sxs-lookup"><span data-stu-id="858c6-188">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="858c6-189">`[CorAllowedOrigin <String[]>]`：取得或設定允許進行交叉起源撥打電話的來源清單 (例如： http://example.com:12345) 。</span><span class="sxs-lookup"><span data-stu-id="858c6-189">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="858c6-190">使用 "\*" 全部允許。</span><span class="sxs-lookup"><span data-stu-id="858c6-190">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="858c6-191">`[CorSupportCredentials <Boolean?>]`：取得或設定是否允許含身分驗證的 CORS 要求。</span><span class="sxs-lookup"><span data-stu-id="858c6-191">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="858c6-192">如需詳細         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         資訊，請參閱。</span><span class="sxs-lookup"><span data-stu-id="858c6-192">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="858c6-193">`[CustomActionExe <String>]`：要執行的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="858c6-193">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="858c6-194">`[CustomActionParameter <String>]`：可執行檔的參數。</span><span class="sxs-lookup"><span data-stu-id="858c6-194">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="858c6-195">`[DefaultDocument <String[]>]`：預設檔。</span><span class="sxs-lookup"><span data-stu-id="858c6-195">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="858c6-196">`[DetailedErrorLoggingEnabled <Boolean?>]`： <code>true</code> 如果已啟用詳細的錯誤記錄，則為（否則，） <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-196">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="858c6-197">`[DocumentRoot <String>]`：檔根。</span><span class="sxs-lookup"><span data-stu-id="858c6-197">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="858c6-198">`[DynamicTagsJson <String>]`：取得或設定一個 JSON 字串，其中包含將從推入註冊端點中的使用者宣告評估的動態標記清單。</span><span class="sxs-lookup"><span data-stu-id="858c6-198">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="858c6-199">`[ExperimentRampUpRule <IRampUpRule[]>]`：提升式規則清單。</span><span class="sxs-lookup"><span data-stu-id="858c6-199">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="858c6-200">`[ActionHostName <String>]`：如果決定要將流量重新導向到的槽主機名稱。</span><span class="sxs-lookup"><span data-stu-id="858c6-200">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="858c6-201">例如.</span><span class="sxs-lookup"><span data-stu-id="858c6-201">E.g.</span></span> <span data-ttu-id="858c6-202">myapp-stage.azurewebsites.net。</span><span class="sxs-lookup"><span data-stu-id="858c6-202">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="858c6-203">`[ChangeDecisionCallbackUrl <String>]`：您可以在 TiPCallback 網站副檔名中提供自訂決策演算法，您可以指定此 URL。</span><span class="sxs-lookup"><span data-stu-id="858c6-203">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="858c6-204">請參閱架設與合約的 TiPCallback 網站延伸。</span><span class="sxs-lookup"><span data-stu-id="858c6-204">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="858c6-205"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="858c6-205">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="858c6-206">`[ChangeIntervalInMinute <Int32?>]`：指定要重新評估 ReroutePercentage 的間隔時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="858c6-206">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="858c6-207">`[ChangeStep <Double?>]`：在自動向上斜坡案例中，這是要新增/移除的步驟， <code>ReroutePercentage</code> 直到到達 \n <code>MinReroutePercentage</code> 或         <code>MaxReroutePercentage</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-207">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="858c6-208">在 .\NCustom 決策演算法中指定的每 N 分鐘數，都 <code>ChangeIntervalInMinutes</code> 可以在 TiPCallback 網站副檔名中提供，您可以在其中指定 URL <code>ChangeDecisionCallbackUrl</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-208">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="858c6-209">`[MaxReroutePercentage <Double?>]`：指定 ReroutePercentage 將持續的上限。</span><span class="sxs-lookup"><span data-stu-id="858c6-209">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="858c6-210">`[MinReroutePercentage <Double?>]`：指定 ReroutePercentage 將持續的較低邊界。</span><span class="sxs-lookup"><span data-stu-id="858c6-210">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="858c6-211">`[Name <String>]`：路由規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="858c6-211">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="858c6-212">建議的名稱是指向將在實驗中接收流量的槽。</span><span class="sxs-lookup"><span data-stu-id="858c6-212">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="858c6-213">`[ReroutePercentage <Double?>]`：將會重新導向之流量的百分比 <code>ActionHostName</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-213">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="858c6-214">`[FtpsState <FtpsState?>]`： FTP/FTPS 服務的狀態</span><span class="sxs-lookup"><span data-stu-id="858c6-214">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="858c6-215">`[HandlerMapping <IHandlerMapping[]>]`：處理常式對應。</span><span class="sxs-lookup"><span data-stu-id="858c6-215">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="858c6-216">`[Argument <String>]`：要傳送至腳本處理器的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="858c6-216">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="858c6-217">`[Extension <String>]`：具有此延伸的要求將會使用指定的 FastCGI 應用程式來處理。</span><span class="sxs-lookup"><span data-stu-id="858c6-217">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="858c6-218">`[ScriptProcessor <String>]`： FastCGI 應用程式的絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="858c6-218">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="858c6-219">`[HealthCheckPath <String>]`：健康情況檢查路徑</span><span class="sxs-lookup"><span data-stu-id="858c6-219">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="858c6-220">`[Http20Enabled <Boolean?>]`： Http20Enabled：將網站設定為允許用戶端經由 HTTP 2.0 連線</span><span class="sxs-lookup"><span data-stu-id="858c6-220">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="858c6-221">`[HttpLoggingEnabled <Boolean?>]`： <code>true</code> 如果已啟用 HTTP 記錄，則為，否則為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-221">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="858c6-222">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`：主要的 IP 安全性限制。</span><span class="sxs-lookup"><span data-stu-id="858c6-222">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="858c6-223">`[Action <String>]`：允許或拒絕此 IP 範圍的存取權。</span><span class="sxs-lookup"><span data-stu-id="858c6-223">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="858c6-224">`[Description <String>]`： IP 限制規則描述。</span><span class="sxs-lookup"><span data-stu-id="858c6-224">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="858c6-225">`[IPAddress <String>]`： [安全性限制] 適用的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="858c6-225">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="858c6-226">它可以是純 ipv4 位址的形式 (必要的 SubnetMask 屬性) 或 CIDR 符號（例如 ipv4/遮罩 (前導位相符）) 。</span><span class="sxs-lookup"><span data-stu-id="858c6-226">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="858c6-227">若是 CIDR，則不得指定 SubnetMask 屬性。</span><span class="sxs-lookup"><span data-stu-id="858c6-227">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="858c6-228">`[Name <String>]`： IP 限制規則名稱。</span><span class="sxs-lookup"><span data-stu-id="858c6-228">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="858c6-229">`[Priority <Int32?>]`： IP 限制規則的優先順序。</span><span class="sxs-lookup"><span data-stu-id="858c6-229">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="858c6-230">`[SubnetMask <String>]`：限制有效的 IP 位址範圍的子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="858c6-230">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="858c6-231">`[SubnetTrafficTag <Int32?>]`： (內部) 子網流量標記</span><span class="sxs-lookup"><span data-stu-id="858c6-231">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="858c6-232">`[Tag <IPFilterTag?>]`：定義此 IP 篩選將用於何種用途。</span><span class="sxs-lookup"><span data-stu-id="858c6-232">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="858c6-233">這是為了支援在 proxy 上進行 IP 篩選。</span><span class="sxs-lookup"><span data-stu-id="858c6-233">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="858c6-234">`[VnetSubnetResourceId <String>]`：虛擬網路資源識別碼</span><span class="sxs-lookup"><span data-stu-id="858c6-234">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="858c6-235">`[VnetTrafficTag <Int32?>]`： (內部) Vnet 流量標記</span><span class="sxs-lookup"><span data-stu-id="858c6-235">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="858c6-236">`[JavaContainer <String>]`： JAVA 容器。</span><span class="sxs-lookup"><span data-stu-id="858c6-236">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="858c6-237">`[JavaContainerVersion <String>]`： JAVA 容器版本。</span><span class="sxs-lookup"><span data-stu-id="858c6-237">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="858c6-238">`[JavaVersion <String>]`： JAVA 版本。</span><span class="sxs-lookup"><span data-stu-id="858c6-238">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="858c6-239">`[LimitMaxDiskSizeInMb <Int64?>]`：允許的磁片大小上限，以 MB 為單位。</span><span class="sxs-lookup"><span data-stu-id="858c6-239">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="858c6-240">`[LimitMaxMemoryInMb <Int64?>]`：允許的最大記憶體使用量（MB）。</span><span class="sxs-lookup"><span data-stu-id="858c6-240">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="858c6-241">`[LimitMaxPercentageCpu <Double?>]`：允許的 CPU 使用量上限百分比。</span><span class="sxs-lookup"><span data-stu-id="858c6-241">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="858c6-242">`[LinuxFxVersion <String>]`： Linux App 架構與版本</span><span class="sxs-lookup"><span data-stu-id="858c6-242">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="858c6-243">`[LoadBalancing <SiteLoadBalancing?>]`：網站負載平衡。</span><span class="sxs-lookup"><span data-stu-id="858c6-243">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="858c6-244">`[LocalMySqlEnabled <Boolean?>]`： <code>true</code> 若要啟用本機 MySQL，否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-244">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="858c6-245">`[LogsDirectorySizeLimit <Int32?>]`： HTTP 記錄目錄大小限制。</span><span class="sxs-lookup"><span data-stu-id="858c6-245">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="858c6-246">`[MachineKeyDecryption <String>]`：用於解密的演算法。</span><span class="sxs-lookup"><span data-stu-id="858c6-246">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="858c6-247">`[MachineKeyDecryptionKey <String>]`：解密金鑰。</span><span class="sxs-lookup"><span data-stu-id="858c6-247">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="858c6-248">`[MachineKeyValidation <String>]`： MachineKey 驗證。</span><span class="sxs-lookup"><span data-stu-id="858c6-248">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="858c6-249">`[MachineKeyValidationKey <String>]`：驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="858c6-249">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="858c6-250">`[ManagedPipelineMode <ManagedPipelineMode?>]`：受管理的管線模式。</span><span class="sxs-lookup"><span data-stu-id="858c6-250">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="858c6-251">`[ManagedServiceIdentityId <Int32?>]`：受管理的服務身分識別識別碼</span><span class="sxs-lookup"><span data-stu-id="858c6-251">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="858c6-252">`[MinTlsVersion <SupportedTlsVersions?>]`： MinTlsVersion：設定 SSL 要求所需的最小 TLS 版本</span><span class="sxs-lookup"><span data-stu-id="858c6-252">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="858c6-253">`[NetFrameworkVersion <String>]`： .NET Framework 版本。</span><span class="sxs-lookup"><span data-stu-id="858c6-253">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="858c6-254">`[NodeVersion <String>]`： Node.js 版本。</span><span class="sxs-lookup"><span data-stu-id="858c6-254">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="858c6-255">`[NumberOfWorker <Int32?>]`：工人的人數。</span><span class="sxs-lookup"><span data-stu-id="858c6-255">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="858c6-256">`[PhpVersion <String>]`： PHP 版本。</span><span class="sxs-lookup"><span data-stu-id="858c6-256">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="858c6-257">`[PowerShellVersion <String>]`： PowerShell 版本。</span><span class="sxs-lookup"><span data-stu-id="858c6-257">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="858c6-258">`[PreWarmedInstanceCount <Int32?>]`： PreWarmed 實例數。</span><span class="sxs-lookup"><span data-stu-id="858c6-258">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="858c6-259">此設定僅適用于消耗量與彈性方案</span><span class="sxs-lookup"><span data-stu-id="858c6-259">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="858c6-260">`[PublishingUsername <String>]`：發佈使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="858c6-260">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="858c6-261">`[PushKind <String>]`：資源類型。</span><span class="sxs-lookup"><span data-stu-id="858c6-261">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="858c6-262">`[PythonVersion <String>]`： Python 版本。</span><span class="sxs-lookup"><span data-stu-id="858c6-262">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="858c6-263">`[RemoteDebuggingEnabled <Boolean?>]`： <code>true</code> 如果已啟用遠端偵錯，則為，否則為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-263">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="858c6-264">`[RemoteDebuggingVersion <String>]`：遠端偵錯版本。</span><span class="sxs-lookup"><span data-stu-id="858c6-264">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="858c6-265">`[RequestCount <Int32?>]`： [要求計數]。</span><span class="sxs-lookup"><span data-stu-id="858c6-265">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="858c6-266">`[RequestTimeInterval <String>]`：時間間隔。</span><span class="sxs-lookup"><span data-stu-id="858c6-266">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="858c6-267">`[RequestTracingEnabled <Boolean?>]`： <code>true</code> 如果已啟用要求追蹤，則為（否則，） <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-267">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="858c6-268">`[RequestTracingExpirationTime <DateTime?>]`：要求追蹤到期時間。</span><span class="sxs-lookup"><span data-stu-id="858c6-268">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="858c6-269">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`：適用于 scm 的 IP 安全性限制。</span><span class="sxs-lookup"><span data-stu-id="858c6-269">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="858c6-270">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`：適用于 scm 的 IP 安全性限制使用 main。</span><span class="sxs-lookup"><span data-stu-id="858c6-270">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="858c6-271">`[ScmType <ScmType?>]`： SCM 類型。</span><span class="sxs-lookup"><span data-stu-id="858c6-271">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="858c6-272">`[SlowRequestCount <Int32?>]`： [要求計數]。</span><span class="sxs-lookup"><span data-stu-id="858c6-272">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="858c6-273">`[SlowRequestTimeInterval <String>]`：時間間隔。</span><span class="sxs-lookup"><span data-stu-id="858c6-273">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="858c6-274">`[SlowRequestTimeTaken <String>]`：拍攝的時間。</span><span class="sxs-lookup"><span data-stu-id="858c6-274">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="858c6-275">`[TagWhitelistJson <String>]`：取得或設定一個 JSON 字串，其中包含由推入註冊端點所使用的白板標記清單。</span><span class="sxs-lookup"><span data-stu-id="858c6-275">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="858c6-276">`[TagsRequiringAuth <String>]`：取得或設定一個 JSON 字串，其中包含需要使用者驗證才能用於推入註冊端點的標記清單。</span><span class="sxs-lookup"><span data-stu-id="858c6-276">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="858c6-277">標記可以由字母數位字元及下列專案所組成：「_ '、' @ '、' # '、'. '、'： '、'-」。</span><span class="sxs-lookup"><span data-stu-id="858c6-277">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="858c6-278">驗證應該在 PushRequestHandler 進行。</span><span class="sxs-lookup"><span data-stu-id="858c6-278">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="858c6-279">`[TracingOption <String>]`：追蹤選項。</span><span class="sxs-lookup"><span data-stu-id="858c6-279">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="858c6-280">`[TriggerPrivateBytesInKb <Int32?>]`：以私人位元組為基礎的規則。</span><span class="sxs-lookup"><span data-stu-id="858c6-280">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="858c6-281">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`：以狀態碼為基礎的規則。</span><span class="sxs-lookup"><span data-stu-id="858c6-281">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="858c6-282">`[Count <Int32?>]`： [要求計數]。</span><span class="sxs-lookup"><span data-stu-id="858c6-282">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="858c6-283">`[Status <Int32?>]`： HTTP 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="858c6-283">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="858c6-284">`[SubStatus <Int32?>]`：要求子狀態。</span><span class="sxs-lookup"><span data-stu-id="858c6-284">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="858c6-285">`[TimeInterval <String>]`：時間間隔。</span><span class="sxs-lookup"><span data-stu-id="858c6-285">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="858c6-286">`[Win32Status <Int32?>]`： Win32 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="858c6-286">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="858c6-287">`[Use32BitWorkerProcess <Boolean?>]`： <code>true</code> 若要使用32位的輔助進程，請按相反的方式 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-287">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="858c6-288">`[VirtualApplication <IVirtualApplication[]>]`：虛擬應用程式。</span><span class="sxs-lookup"><span data-stu-id="858c6-288">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="858c6-289">`[PhysicalPath <String>]`：實體路徑。</span><span class="sxs-lookup"><span data-stu-id="858c6-289">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="858c6-290">`[PreloadEnabled <Boolean?>]`： <code>true</code> 如果已啟用預載入，則為，否則為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-290">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="858c6-291">`[VirtualDirectory <IVirtualDirectory[]>]`：虛擬應用程式的虛擬目錄。</span><span class="sxs-lookup"><span data-stu-id="858c6-291">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="858c6-292">`[PhysicalPath <String>]`：實體路徑。</span><span class="sxs-lookup"><span data-stu-id="858c6-292">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="858c6-293">`[VirtualPath <String>]`：虛擬應用程式的路徑。</span><span class="sxs-lookup"><span data-stu-id="858c6-293">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="858c6-294">`[VirtualPath <String>]`：虛擬路徑。</span><span class="sxs-lookup"><span data-stu-id="858c6-294">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="858c6-295">`[VnetName <String>]`：虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="858c6-295">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="858c6-296">`[WebSocketsEnabled <Boolean?>]`： <code>true</code> 如果已啟用 WebSocket，則為，否則為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-296">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="858c6-297">`[WindowsFxVersion <String>]`： Xenon 應用程式架構與版本</span><span class="sxs-lookup"><span data-stu-id="858c6-297">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="858c6-298">`[XManagedServiceIdentityId <Int32?>]`：顯式管理的服務身分識別識別碼</span><span class="sxs-lookup"><span data-stu-id="858c6-298">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="858c6-299">`[ContainerSize <Int32?>]`：函數容器的大小。</span><span class="sxs-lookup"><span data-stu-id="858c6-299">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="858c6-300">`[DailyMemoryTimeQuota <Int32?>]`： (僅適用于動態 app 的 [允許的每日記憶體時間配額限制]) 。</span><span class="sxs-lookup"><span data-stu-id="858c6-300">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="858c6-301">`[Enabled <Boolean?>]`： <code>true</code> 如果已啟用應用程式，否則為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-301">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="858c6-302">將此值設定為 false 會停用 app (將 app 離線) 。</span><span class="sxs-lookup"><span data-stu-id="858c6-302">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="858c6-303">`[HostNameSslState <IHostNameSslState[]>]`：主機名稱 SSL 狀態是用來管理 app 主機名稱的 SSL 系結。</span><span class="sxs-lookup"><span data-stu-id="858c6-303">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="858c6-304">`[HostType <HostType?>]`：表示主機名稱是標準版還是知識庫主機名稱。</span><span class="sxs-lookup"><span data-stu-id="858c6-304">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="858c6-305">`[Name <String>]`主機.</span><span class="sxs-lookup"><span data-stu-id="858c6-305">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="858c6-306">`[SslState <SslState?>]`： SSL 類型。</span><span class="sxs-lookup"><span data-stu-id="858c6-306">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="858c6-307">`[Thumbprint <String>]`： SSL 憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="858c6-307">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="858c6-308">`[ToUpdate <Boolean?>]`：設定為 <code>true</code> 以更新現有的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="858c6-308">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="858c6-309">`[VirtualIP <String>]`：如果啟用 IP SSL，則會指派給主機名稱的虛擬 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="858c6-309">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="858c6-310">`[HostNamesDisabled <Boolean?>]`： <code>true</code> 若要停用應用程式的公用主機名稱，否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-310">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="858c6-311">如果 <code>true</code> 是，只能透過 API 管理程式存取 app。</span><span class="sxs-lookup"><span data-stu-id="858c6-311">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="858c6-312">`[HostingEnvironmentProfileId <String>]`：應用程式服務環境的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="858c6-312">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="858c6-313">`[HttpsOnly <Boolean?>]`： HttpsOnly：將網站配置為只接受 HTTPs 要求。</span><span class="sxs-lookup"><span data-stu-id="858c6-313">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="858c6-314">Http 要求的重新導向問題</span><span class="sxs-lookup"><span data-stu-id="858c6-314">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="858c6-315">`[HyperV <Boolean?>]`： Hyper-v 沙箱。</span><span class="sxs-lookup"><span data-stu-id="858c6-315">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="858c6-316">`[IdentityType <ManagedServiceIdentityType?>]`：受管理的服務身分識別類型。</span><span class="sxs-lookup"><span data-stu-id="858c6-316">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="858c6-317">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`：指派與資源相關聯之身分識別的使用者清單。</span><span class="sxs-lookup"><span data-stu-id="858c6-317">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="858c6-318">使用者身分識別字典金鑰參照會是下列形式的 ARM 資源識別碼： '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span><span class="sxs-lookup"><span data-stu-id="858c6-318">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="858c6-319">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="858c6-319">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="858c6-320">`[IsXenon <Boolean?>]`：已過時： Hyper-v 沙箱。</span><span class="sxs-lookup"><span data-stu-id="858c6-320">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="858c6-321">`[RedundancyMode <RedundancyMode?>]`：網站冗余模式</span><span class="sxs-lookup"><span data-stu-id="858c6-321">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="858c6-322">`[Reserved <Boolean?>]`： <code>true</code> 如果保留，則為，否則， <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-322">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="858c6-323">`[ScmSiteAlsoStopped <Boolean?>]`： <code>true</code> 若要在應用程式停止時停止 SCM (KUDU) 網站，請按相反步驟操作 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-323">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="858c6-324">預設值為 <code>false</code> 。</span><span class="sxs-lookup"><span data-stu-id="858c6-324">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="858c6-325">`[ServerFarmId <String>]`：相關應用程式服務方案的資源識別碼，格式為： "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}"。</span><span class="sxs-lookup"><span data-stu-id="858c6-325">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="858c6-326">相關連結</span><span class="sxs-lookup"><span data-stu-id="858c6-326">RELATED LINKS</span></span>

