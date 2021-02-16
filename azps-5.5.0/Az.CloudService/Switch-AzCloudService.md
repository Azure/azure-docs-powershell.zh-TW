---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/Switch-AzCloudService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
ms.openlocfilehash: f10d11dbbe98c098286a072d5882bf5d3a464d8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136571"
---
# <span data-ttu-id="ea9bf-101">Switch-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="ea9bf-101">Switch-AzCloudService</span></span>

## <span data-ttu-id="ea9bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ea9bf-102">SYNOPSIS</span></span>
<span data-ttu-id="ea9bf-103">在兩個雲端服務 (延伸支援) 負載平衡器之間交換 Vip。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-103">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

## <span data-ttu-id="ea9bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="ea9bf-104">SYNTAX</span></span>

### <span data-ttu-id="ea9bf-105">CloudServiceName (預設) </span><span class="sxs-lookup"><span data-stu-id="ea9bf-105">CloudServiceName (Default)</span></span>
```
Switch-AzCloudService -CloudServiceName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Async] [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ea9bf-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="ea9bf-106">CloudService</span></span>
```
Switch-AzCloudService -CloudService <CloudService> [-SubscriptionId <String>] [-Async]
 [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ea9bf-107">說明</span><span class="sxs-lookup"><span data-stu-id="ea9bf-107">DESCRIPTION</span></span>
<span data-ttu-id="ea9bf-108">在兩個雲端服務 (延伸支援) 負載平衡器之間交換 Vip。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-108">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

## <span data-ttu-id="ea9bf-109">示例</span><span class="sxs-lookup"><span data-stu-id="ea9bf-109">EXAMPLES</span></span>

### <span data-ttu-id="ea9bf-110">範例1：使用名稱切換雲端服務</span><span class="sxs-lookup"><span data-stu-id="ea9bf-110">Example 1: Switch cloud service using name</span></span>
```powershell
PS C:\> Switch-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="ea9bf-111">上述命令會在名為「BService」的雲端服務上執行 vipswap 作業，並會在使用者在確認提示字元上確認該動作之後，才會執行該作業。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-111">Above command invokes the vipswap operation on the Cloud service with name 'BService' and will perform the operation once the user confirms the action on the confirmation prompt.</span></span>
<span data-ttu-id="ea9bf-112">[BService]，並以其可交換的雲端服務進行交換。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-112">'BService' with be swapped with its swappable cloud service.</span></span>

### <span data-ttu-id="ea9bf-113">範例2：使用雲端服務物件切換雲端服務</span><span class="sxs-lookup"><span data-stu-id="ea9bf-113">Example 2: Switch cloud service using cloud service object</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Switch-AzCloudService -CloudService $cs

```

<span data-ttu-id="ea9bf-114">上述命令會在名為「BService」的雲端服務上執行 vipswap 作業，並會在使用者在確認提示字元上確認該動作之後，才會執行該作業。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-114">Above command invokes the vipswap operation on the Cloud service with name 'BService' and will perform the operation once the user confirms the action on the confirmation prompt.</span></span>
<span data-ttu-id="ea9bf-115">[BService]，並以其可交換的雲端服務進行交換。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-115">'BService' with be swapped with its swappable cloud service.</span></span>

## <span data-ttu-id="ea9bf-116">參數</span><span class="sxs-lookup"><span data-stu-id="ea9bf-116">PARAMETERS</span></span>

### <span data-ttu-id="ea9bf-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea9bf-117">-AsJob</span></span>
<span data-ttu-id="ea9bf-118">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="ea9bf-118">Run the command as a job</span></span>

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

### <span data-ttu-id="ea9bf-119">-Async</span><span class="sxs-lookup"><span data-stu-id="ea9bf-119">-Async</span></span>


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

### <span data-ttu-id="ea9bf-120">-CloudService</span><span class="sxs-lookup"><span data-stu-id="ea9bf-120">-CloudService</span></span>
<span data-ttu-id="ea9bf-121">若要建立，請參閱 CLOUDSERVICE 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-121">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudService
Parameter Sets: CloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea9bf-122">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="ea9bf-122">-CloudServiceName</span></span>


```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea9bf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea9bf-123">-DefaultProfile</span></span>
<span data-ttu-id="ea9bf-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea9bf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea9bf-125">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea9bf-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea9bf-126">-SubscriptionId</span></span>
<span data-ttu-id="ea9bf-127">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ea9bf-128">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea9bf-129">-確認</span><span class="sxs-lookup"><span data-stu-id="ea9bf-129">-Confirm</span></span>
<span data-ttu-id="ea9bf-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea9bf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea9bf-131">-WhatIf</span></span>
<span data-ttu-id="ea9bf-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea9bf-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea9bf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea9bf-134">CommonParameters</span></span>
<span data-ttu-id="ea9bf-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea9bf-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea9bf-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ea9bf-137">INPUTS</span></span>

## <span data-ttu-id="ea9bf-138">輸出</span><span class="sxs-lookup"><span data-stu-id="ea9bf-138">OUTPUTS</span></span>

### <span data-ttu-id="ea9bf-139">System.object</span><span class="sxs-lookup"><span data-stu-id="ea9bf-139">System.Boolean</span></span>

## <span data-ttu-id="ea9bf-140">筆記</span><span class="sxs-lookup"><span data-stu-id="ea9bf-140">NOTES</span></span>

<span data-ttu-id="ea9bf-141">別名</span><span class="sxs-lookup"><span data-stu-id="ea9bf-141">ALIASES</span></span>

<span data-ttu-id="ea9bf-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ea9bf-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ea9bf-143">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ea9bf-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ea9bf-145">CLOUDSERVICE <CloudService> ：</span><span class="sxs-lookup"><span data-stu-id="ea9bf-145">CLOUDSERVICE <CloudService>:</span></span> 
  - <span data-ttu-id="ea9bf-146">`Location <String>`：資源位置。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-146">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="ea9bf-147">`[Configuration <String>]`：指定雲端服務的 XML 服務配置 ( .cscfg) 。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-147">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="ea9bf-148">`[ConfigurationUrl <String>]`：指定在 Blob 服務中參照服務配置位置的 URL。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-148">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="ea9bf-149">您可以從任何儲存空間帳戶 (SAS) URI，以共用存取簽章的服務套件 URL。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-149">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="ea9bf-150">這是只寫屬性，不會在 [取得呼叫] 中傳回。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-150">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="ea9bf-151">`[ExtensionProfile <ICloudServiceExtensionProfile>]`：說明雲端服務延伸設定檔。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-151">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="ea9bf-152">`[Extension <IExtension[]>]`：雲端服務的延伸清單。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-152">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="ea9bf-153">`[AutoUpgradeMinorVersion <Boolean?>]`：明確指定平臺在可用時是否可自動將 typeHandlerVersion 升級至較高的次要版本。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-153">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="ea9bf-154">`[ForceUpdateTag <String>]`：標記以強制套用提供的公用和受保護設定。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-154">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="ea9bf-155">變更 tag 值可讓您重新執行延伸，而不需變更任何公用或受保護的設定。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-155">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="ea9bf-156">如果 forceUpdateTag 未變更，則處理常式仍會套用對公眾或受保護設定的更新。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-156">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="ea9bf-157">如果沒有 forceUpdateTag，也不會變更任何公開或受保護的設定，延伸將會以相同的序號碼流向角色實例，而不論是否重新執行，都可以使用處理程式的實現</span><span class="sxs-lookup"><span data-stu-id="ea9bf-157">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="ea9bf-158">`[Name <String>]`：延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-158">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="ea9bf-159">`[ProtectedSetting <String>]`：已在傳送至角色實例之前加密之副檔名的受保護設定。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-159">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="ea9bf-160">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="ea9bf-160">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="ea9bf-161">`[Publisher <String>]`：延伸處理常式發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-161">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="ea9bf-162">`[RolesAppliedTo <String[]>]`：選用的角色清單來套用此延伸。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-162">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="ea9bf-163">如果未指定屬性或指定了 ' \*」，則會將延伸套用到雲端服務中的所有角色。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-163">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="ea9bf-164">`[Setting <String>]`：延伸的公開設定。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-164">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="ea9bf-165">對於 JSON 延伸，這是延伸的 JSON 設定。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-165">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="ea9bf-166">針對 XML 延伸 (例如 RDP) ，這是延伸的 XML 設定。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-166">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="ea9bf-167">`[SourceVaultId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ea9bf-167">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="ea9bf-168">`[Type <String>]`：指定延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-168">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="ea9bf-169">`[TypeHandlerVersion <String>]`：指定延伸的版本。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-169">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="ea9bf-170">指定副檔名的版本。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-170">Specifies the version of the extension.</span></span> <span data-ttu-id="ea9bf-171">如果未指定此元素，或使用星號 ( \* ) 作為值，就會使用最新的延伸版本。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-171">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="ea9bf-172">如果將該值指定為主要版本號碼，並以星號做為次要版本號碼 (X. ) ，則會選取指定主要版本的最新次要版本。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-172">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="ea9bf-173">如果 (X-y) 指定主要版本號碼和次要版本號碼，則會選取特定副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-173">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="ea9bf-174">如果指定版本，則會在角色實例上執行自動升級。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-174">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="ea9bf-175">`[NetworkProfile <ICloudServiceNetworkProfile>]`：雲端服務的網路設定檔。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-175">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="ea9bf-176">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`：雲端服務的負載平衡器設定清單。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-176">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="ea9bf-177">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`： IP 清單</span><span class="sxs-lookup"><span data-stu-id="ea9bf-177">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="ea9bf-178">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="ea9bf-178">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="ea9bf-179">`[PrivateIPAddress <String>]`：雲端服務所參照的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-179">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="ea9bf-180">`[PublicIPAddressId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ea9bf-180">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="ea9bf-181">`[SubnetId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ea9bf-181">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="ea9bf-182">`[Name <String>]`：資源名稱</span><span class="sxs-lookup"><span data-stu-id="ea9bf-182">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="ea9bf-183">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="ea9bf-183">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="ea9bf-184">`[Id <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ea9bf-184">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="ea9bf-185">`[OSProfile <ICloudServiceOSProfile>]`：說明雲端服務的 OS 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-185">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="ea9bf-186">`[Secret <ICloudServiceVaultSecretGroup[]>]`：指定應該安裝在角色實例上的憑證集合。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-186">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="ea9bf-187">`[SourceVaultId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ea9bf-187">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="ea9bf-188">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`： SourceVault 中包含憑證的主要保存庫參照清單。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-188">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="ea9bf-189">`[CertificateUrl <String>]`：這是已上傳到金鑰保存庫的憑證 URL （密碼）。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-189">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="ea9bf-190">`[PackageUrl <String>]`：指定要參照 Blob 服務中服務套件位置的 URL。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-190">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="ea9bf-191">您可以從任何儲存空間帳戶 (SAS) URI，以共用存取簽章的服務套件 URL。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-191">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="ea9bf-192">這是只寫屬性，不會在 [取得呼叫] 中傳回。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-192">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="ea9bf-193">`[RoleProfile <ICloudServiceRoleProfile>]`：說明雲端服務的角色設定檔。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-193">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="ea9bf-194">`[Role <ICloudServiceRoleProfileProperties[]>]`：雲端服務的角色清單。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-194">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="ea9bf-195">`[Name <String>]`：資源名稱。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-195">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="ea9bf-196">`[SkuCapacity <Int64?>]`：指定雲端服務中的角色實例數。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-196">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="ea9bf-197">`[SkuName <String>]`： Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-197">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="ea9bf-198">注意：如果雲端服務目前所在的硬體不支援新版 SKU，您必須刪除並重新建立雲端服務，或移回舊版 SKU。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-198">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="ea9bf-199">`[SkuTier <String>]`：指定雲端服務的層級。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-199">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="ea9bf-200">可能的值為</span><span class="sxs-lookup"><span data-stu-id="ea9bf-200">Possible Values are</span></span> <br /><br /> <span data-ttu-id="ea9bf-201">**標準**</span><span class="sxs-lookup"><span data-stu-id="ea9bf-201">**Standard**</span></span> <br /><br /> <span data-ttu-id="ea9bf-202">**空白**</span><span class="sxs-lookup"><span data-stu-id="ea9bf-202">**Basic**</span></span>
  - <span data-ttu-id="ea9bf-203">`[StartCloudService <Boolean?>]`： (選用) 指出是否要在建立雲端服務後立即啟動。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-203">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="ea9bf-204">預設值為 `true` 。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-204">The default value is `true`.</span></span>         <span data-ttu-id="ea9bf-205">如果是 false，則表示服務模型仍在部署，但程式碼不會立即執行。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-205">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="ea9bf-206">相反地，服務會在您呼叫 Start 之前 PoweredOff，直到該服務開始時才會啟動。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-206">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="ea9bf-207">即使是 poweredoff，部署的服務仍會產生費用。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-207">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="ea9bf-208">`[Tag <ICloudServiceTags>]`：資源標記。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-208">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="ea9bf-209">`[(Any) <String>]`：這表示您可以將任何屬性新增至此物件。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-209">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="ea9bf-210">`[UpgradeMode <CloudServiceUpgradeMode?>]`：雲端服務的更新模式。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-210">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="ea9bf-211">部署服務時，系統會將角色實例指派給更新網域。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-211">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="ea9bf-212">更新可以在每個更新網域中手動啟動，或是在所有更新網域中自動啟動。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-212">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="ea9bf-213">可能的值為</span><span class="sxs-lookup"><span data-stu-id="ea9bf-213">Possible Values are</span></span> <br /><br /><span data-ttu-id="ea9bf-214">**自動**</span><span class="sxs-lookup"><span data-stu-id="ea9bf-214">**Auto**</span></span><br /><br /><span data-ttu-id="ea9bf-215">**手動**</span><span class="sxs-lookup"><span data-stu-id="ea9bf-215">**Manual**</span></span> <br /><br /><span data-ttu-id="ea9bf-216">**辦公**</span><span class="sxs-lookup"><span data-stu-id="ea9bf-216">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="ea9bf-217">如果沒有指定，則預設值為 Auto。如果設定為 [手動]，則必須呼叫 UpdateDomain，才能套用更新。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-217">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="ea9bf-218">如果設為 Auto，更新會自動套用至每個更新網域。</span><span class="sxs-lookup"><span data-stu-id="ea9bf-218">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="ea9bf-219">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea9bf-219">RELATED LINKS</span></span>

