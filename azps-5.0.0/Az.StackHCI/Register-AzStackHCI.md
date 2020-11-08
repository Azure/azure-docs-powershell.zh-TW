---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: c09c4b4c8d71d90bbbac0771c75ea3ea51ee05dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138639"
---
# <span data-ttu-id="887ff-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="887ff-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="887ff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="887ff-102">SYNOPSIS</span></span>
<span data-ttu-id="887ff-103">Register-AzStackHCI 會建立代表內部部署群集的 AzureStackHCI 雲端資源，並使用 Azure 註冊內部部署的群集。</span><span class="sxs-lookup"><span data-stu-id="887ff-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="887ff-104">句法</span><span class="sxs-lookup"><span data-stu-id="887ff-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="887ff-105">說明</span><span class="sxs-lookup"><span data-stu-id="887ff-105">DESCRIPTION</span></span>
<span data-ttu-id="887ff-106">Register-AzStackHCI 會建立代表內部部署群集的 AzureStackHCI 雲端資源，並使用 Azure 註冊內部部署的群集。</span><span class="sxs-lookup"><span data-stu-id="887ff-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="887ff-107">示例</span><span class="sxs-lookup"><span data-stu-id="887ff-107">EXAMPLES</span></span>

### <span data-ttu-id="887ff-108">範例1</span><span class="sxs-lookup"><span data-stu-id="887ff-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node.
```

<span data-ttu-id="887ff-109">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" 結果：成功的 ResourceId：/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview ： PortalAADAppPermissionsURL： https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="887ff-109">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span></span>

### <span data-ttu-id="887ff-110">範例2</span><span class="sxs-lookup"><span data-stu-id="887ff-110">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="887ff-111">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ComputerName ClusterNode1 結果：成功的 ResourceId：/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL： https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL： https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="887ff-111">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="887ff-112">範例3</span><span class="sxs-lookup"><span data-stu-id="887ff-112">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="887ff-113">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer .。。ere =-GraphAccessToken acyee。rerrer- user1@corp1.com Region westus-ResourceGroupName DemoHCICluster3-DemoHCIRG 結果： PendingForAdminConsent ResourceId：/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL： https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL： https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="887ff-113">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="887ff-114">範例4</span><span class="sxs-lookup"><span data-stu-id="887ff-114">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="887ff-115">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-地區 westus HciCluster1-TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer .。。ere =-GraphAccessToken acee。rerrer- user1@corp1.com EnvironmentName AzureCloud-ComputerName node1hci-認證 Get-Credential 結果：成功的 ResourceId：/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL： https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL： https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="887ff-115">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

## <span data-ttu-id="887ff-116">參數</span><span class="sxs-lookup"><span data-stu-id="887ff-116">PARAMETERS</span></span>

### <span data-ttu-id="887ff-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="887ff-117">-SubscriptionId</span></span>
<span data-ttu-id="887ff-118">指定要建立資源的 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="887ff-118">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="887ff-119">這是唯一的強制參數。</span><span class="sxs-lookup"><span data-stu-id="887ff-119">This is the only Mandatory parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="887ff-120">-Region</span><span class="sxs-lookup"><span data-stu-id="887ff-120">-Region</span></span>
<span data-ttu-id="887ff-121">指定要建立資源的區域。</span><span class="sxs-lookup"><span data-stu-id="887ff-121">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="887ff-122">預設值為 EastUS。</span><span class="sxs-lookup"><span data-stu-id="887ff-122">Default is EastUS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="887ff-123">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="887ff-123">-ResourceName</span></span>
<span data-ttu-id="887ff-124">指定在 Azure 中建立之資源的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="887ff-124">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="887ff-125">如果沒有指定，則會使用內部部署的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="887ff-125">If not specified, on-premise cluster name is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="887ff-126">-TenantId</span><span class="sxs-lookup"><span data-stu-id="887ff-126">-TenantId</span></span>
<span data-ttu-id="887ff-127">指定 Azure TenantId。</span><span class="sxs-lookup"><span data-stu-id="887ff-127">Specifies the Azure TenantId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="887ff-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="887ff-128">-ResourceGroupName</span></span>
<span data-ttu-id="887ff-129">指定 Azure 資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="887ff-129">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="887ff-130">如果沒有指定 \<LocalClusterName\> ，則會將 rg 用作資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="887ff-130">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="887ff-131">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="887ff-131">-ArmAccessToken</span></span>
<span data-ttu-id="887ff-132">指定 ARM 存取權杖。</span><span class="sxs-lookup"><span data-stu-id="887ff-132">Specifies the ARM access token.</span></span>
<span data-ttu-id="887ff-133">將此指定與 GraphAccessToken 和 AccountId 搭配使用，就可以避免 Azure 互動式登入。</span><span class="sxs-lookup"><span data-stu-id="887ff-133">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="887ff-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="887ff-134">-GraphAccessToken</span></span>
<span data-ttu-id="887ff-135">指定圖形存取權杖。</span><span class="sxs-lookup"><span data-stu-id="887ff-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="887ff-136">將此指定與 ArmAccessToken 和 AccountId 搭配使用，就可以避免 Azure 互動式登入。</span><span class="sxs-lookup"><span data-stu-id="887ff-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="887ff-137">-AccountId</span><span class="sxs-lookup"><span data-stu-id="887ff-137">-AccountId</span></span>
<span data-ttu-id="887ff-138">指定 ARM 存取權杖。</span><span class="sxs-lookup"><span data-stu-id="887ff-138">Specifies the ARM access token.</span></span>
<span data-ttu-id="887ff-139">將它與 ArmAccessToken 和 GraphAccessToken 一起指定，將會避開 Azure 互動式登入。</span><span class="sxs-lookup"><span data-stu-id="887ff-139">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="887ff-140">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="887ff-140">-EnvironmentName</span></span>
<span data-ttu-id="887ff-141">指定 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="887ff-141">Specifies the Azure Environment.</span></span>
<span data-ttu-id="887ff-142">預設值為 AzureCloud。</span><span class="sxs-lookup"><span data-stu-id="887ff-142">Default is AzureCloud.</span></span>
<span data-ttu-id="887ff-143">有效值為 AzureCloud、AzureChinaCloud、AzureUSGovernment、AzureGermanCloud、AzurePPE</span><span class="sxs-lookup"><span data-stu-id="887ff-143">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="887ff-144">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="887ff-144">-ComputerName</span></span>
<span data-ttu-id="887ff-145">指定群集名稱或內部部署群集中要註冊至 Azure 的叢集節點之一。</span><span class="sxs-lookup"><span data-stu-id="887ff-145">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="887ff-146">-認證</span><span class="sxs-lookup"><span data-stu-id="887ff-146">-Credential</span></span>
<span data-ttu-id="887ff-147">指定 ComputerName 的認證。</span><span class="sxs-lookup"><span data-stu-id="887ff-147">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="887ff-148">[預設值] 是執行 Cmdlet 的目前使用者。</span><span class="sxs-lookup"><span data-stu-id="887ff-148">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="887ff-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="887ff-149">CommonParameters</span></span>
<span data-ttu-id="887ff-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="887ff-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="887ff-151">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="887ff-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="887ff-152">輸入</span><span class="sxs-lookup"><span data-stu-id="887ff-152">INPUTS</span></span>

## <span data-ttu-id="887ff-153">輸出</span><span class="sxs-lookup"><span data-stu-id="887ff-153">OUTPUTS</span></span>

### <span data-ttu-id="887ff-154">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="887ff-154">PSCustomObject.</span></span> <span data-ttu-id="887ff-155">在 PSCustomObject 中傳回下列屬性</span><span class="sxs-lookup"><span data-stu-id="887ff-155">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="887ff-156">結果：成功或失敗，或 PendingForAdminConsent 或取消。</span><span class="sxs-lookup"><span data-stu-id="887ff-156">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="887ff-157">ResourceId：在 Azure 中建立之資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="887ff-157">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="887ff-158">PortalResourceURL： Azure 入口網站資源 URL。</span><span class="sxs-lookup"><span data-stu-id="887ff-158">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="887ff-159">PortalAADAppPermissionsURL： AAD App 許可權頁面的 Azure 入口網站 URL。</span><span class="sxs-lookup"><span data-stu-id="887ff-159">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="887ff-160">筆記</span><span class="sxs-lookup"><span data-stu-id="887ff-160">NOTES</span></span>

## <span data-ttu-id="887ff-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="887ff-161">RELATED LINKS</span></span>
