---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: 2a6e94512e8bc9bed980c76b5430118d74bd3f6d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910914"
---
# <span data-ttu-id="802c6-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="802c6-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="802c6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="802c6-102">SYNOPSIS</span></span>
<span data-ttu-id="802c6-103">Register-AzStackHCI建立代表內部部署組群的 Microsoft.AzureStackHCI 雲端資源，然後向 Azure 登錄內部部署組。</span><span class="sxs-lookup"><span data-stu-id="802c6-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="802c6-104">語法</span><span class="sxs-lookup"><span data-stu-id="802c6-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-CertificateThumbprint] <String>] [-RepairRegistration]
 [-UseDeviceAuthentication] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="802c6-105">描述</span><span class="sxs-lookup"><span data-stu-id="802c6-105">DESCRIPTION</span></span>
<span data-ttu-id="802c6-106">Register-AzStackHCI建立代表內部部署組群的 Microsoft.AzureStackHCI 雲端資源，然後向 Azure 登錄內部部署組。</span><span class="sxs-lookup"><span data-stu-id="802c6-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="802c6-107">例子</span><span class="sxs-lookup"><span data-stu-id="802c6-107">EXAMPLES</span></span>

### <span data-ttu-id="802c6-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="802c6-108">EXAMPLE 1</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" 
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/
```

<span data-ttu-id="802c6-109">其中一個組節點上啟動。</span><span class="sxs-lookup"><span data-stu-id="802c6-109">Invoking on one of the cluster node.</span></span>

### <span data-ttu-id="802c6-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="802c6-110">EXAMPLE 2</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="802c6-111">從管理節點中啟動。</span><span class="sxs-lookup"><span data-stu-id="802c6-111">Invoking from the management node.</span></span>

### <span data-ttu-id="802c6-112">範例 3</span><span class="sxs-lookup"><span data-stu-id="802c6-112">EXAMPLE 3</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG 
Result: PendingForAdminConsent
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="802c6-113">從 WAC 中引文。</span><span class="sxs-lookup"><span data-stu-id="802c6-113">Invoking from WAC.</span></span>

### <span data-ttu-id="802c6-114">範例 4</span><span class="sxs-lookup"><span data-stu-id="802c6-114">EXAMPLE 4</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="802c6-115">使用所有參數來引用。</span><span class="sxs-lookup"><span data-stu-id="802c6-115">Invoking with all the parameters.</span></span>

## <span data-ttu-id="802c6-116">參數</span><span class="sxs-lookup"><span data-stu-id="802c6-116">PARAMETERS</span></span>

### <span data-ttu-id="802c6-117">-AccountId</span><span class="sxs-lookup"><span data-stu-id="802c6-117">-AccountId</span></span>
<span data-ttu-id="802c6-118">指定 ARM 存取權杖。</span><span class="sxs-lookup"><span data-stu-id="802c6-118">Specifies the ARM access token.</span></span>
<span data-ttu-id="802c6-119">在 ArmAccessToken 和 GraphAccessToken 中指定此選項可避免 Azure 互動式登入。</span><span class="sxs-lookup"><span data-stu-id="802c6-119">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802c6-120">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="802c6-120">-ArmAccessToken</span></span>
<span data-ttu-id="802c6-121">指定 ARM 存取權杖。</span><span class="sxs-lookup"><span data-stu-id="802c6-121">Specifies the ARM access token.</span></span>
<span data-ttu-id="802c6-122">與 GraphAccessToken 和 AccountId 一起指定此選項可避免 Azure 互動式登入。</span><span class="sxs-lookup"><span data-stu-id="802c6-122">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802c6-123">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="802c6-123">-CertificateThumbprint</span></span>
<span data-ttu-id="802c6-124">指定所有節點上可用憑證的指紋。</span><span class="sxs-lookup"><span data-stu-id="802c6-124">Specifies the thumbprint of the certificate available on all the nodes.</span></span> <span data-ttu-id="802c6-125">使用者負責管理憑證。</span><span class="sxs-lookup"><span data-stu-id="802c6-125">User is responsible for managing the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802c6-126">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="802c6-126">-ComputerName</span></span>
<span data-ttu-id="802c6-127">指定要註冊至 Azure 之內部部署組集中的組名或其中一個集區節點。</span><span class="sxs-lookup"><span data-stu-id="802c6-127">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802c6-128">-認證</span><span class="sxs-lookup"><span data-stu-id="802c6-128">-Credential</span></span>
<span data-ttu-id="802c6-129">指定 ComputerName 的認證。</span><span class="sxs-lookup"><span data-stu-id="802c6-129">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="802c6-130">預設值為執行 Cmdlet 的目前使用者。</span><span class="sxs-lookup"><span data-stu-id="802c6-130">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802c6-131">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="802c6-131">-EnvironmentName</span></span>
<span data-ttu-id="802c6-132">指定 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="802c6-132">Specifies the Azure Environment.</span></span>
<span data-ttu-id="802c6-133">預設值為 AzureCloud。</span><span class="sxs-lookup"><span data-stu-id="802c6-133">Default is AzureCloud.</span></span>
<span data-ttu-id="802c6-134">有效的值為 AzureCloud、AzureChinaCloud、AzureUSGovernment、AzureGermanCloud、AzurePPE</span><span class="sxs-lookup"><span data-stu-id="802c6-134">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802c6-135">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="802c6-135">-GraphAccessToken</span></span>
<span data-ttu-id="802c6-136">指定 Graph 存取權杖。</span><span class="sxs-lookup"><span data-stu-id="802c6-136">Specifies the Graph access token.</span></span>
<span data-ttu-id="802c6-137">在 ArmAccessToken 和 AccountId 中指定此選項可避免 Azure 互動式登入。</span><span class="sxs-lookup"><span data-stu-id="802c6-137">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802c6-138">-區域</span><span class="sxs-lookup"><span data-stu-id="802c6-138">-Region</span></span>
<span data-ttu-id="802c6-139">指定要建立資源的地區。</span><span class="sxs-lookup"><span data-stu-id="802c6-139">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="802c6-140">預設值為 EastUS。</span><span class="sxs-lookup"><span data-stu-id="802c6-140">Default is EastUS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802c6-141">-RepairRegistration</span><span class="sxs-lookup"><span data-stu-id="802c6-141">-RepairRegistration</span></span>
<span data-ttu-id="802c6-142">使用雲端修復目前的 Azure Stack HCI 註冊。</span><span class="sxs-lookup"><span data-stu-id="802c6-142">Repair the current Azure Stack HCI registration with the cloud.</span></span> <span data-ttu-id="802c6-143">此 Cmdlet 會刪除集區節點上的本地憑證，以及雲端 Azure AD 應用程式中的遠端憑證，並產生兩者的新取代憑證。</span><span class="sxs-lookup"><span data-stu-id="802c6-143">This cmdlet deletes the local certificates on the clustered nodes and the remote certificates in the Azure AD application in the cloud and generates new replacement certificates for both.</span></span> <span data-ttu-id="802c6-144">資源群組、資源名稱及其他註冊選項會保留。</span><span class="sxs-lookup"><span data-stu-id="802c6-144">The resource group, resource name, and other registration choices are preserved.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802c6-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="802c6-145">-ResourceGroupName</span></span>
<span data-ttu-id="802c6-146">指定 Azure 資源組名。</span><span class="sxs-lookup"><span data-stu-id="802c6-146">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="802c6-147">如果未指定 \<LocalClusterName\> -rg，將會使用做為資源組名。</span><span class="sxs-lookup"><span data-stu-id="802c6-147">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802c6-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="802c6-148">-ResourceName</span></span>
<span data-ttu-id="802c6-149">指定在 Azure 中建立之資源的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="802c6-149">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="802c6-150">如果未指定，會使用內部部署組名。</span><span class="sxs-lookup"><span data-stu-id="802c6-150">If not specified, on-premise cluster name is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802c6-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="802c6-151">-SubscriptionId</span></span>
<span data-ttu-id="802c6-152">指定 Azure 訂閱以建立資源。</span><span class="sxs-lookup"><span data-stu-id="802c6-152">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="802c6-153">這是唯一的強制參數。</span><span class="sxs-lookup"><span data-stu-id="802c6-153">This is the only Mandatory parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802c6-154">-TenantId</span><span class="sxs-lookup"><span data-stu-id="802c6-154">-TenantId</span></span>
<span data-ttu-id="802c6-155">指定 Azure TenantId。</span><span class="sxs-lookup"><span data-stu-id="802c6-155">Specifies the Azure TenantId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802c6-156">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="802c6-156">-UseDeviceAuthentication</span></span>
<span data-ttu-id="802c6-157">使用裝置代碼驗證，而不使用互動式瀏覽器提示。</span><span class="sxs-lookup"><span data-stu-id="802c6-157">Use device code authentication instead of an interactive browser prompt.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802c6-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="802c6-158">CommonParameters</span></span>
<span data-ttu-id="802c6-159">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="802c6-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="802c6-160">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="802c6-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="802c6-161">輸入</span><span class="sxs-lookup"><span data-stu-id="802c6-161">INPUTS</span></span>

## <span data-ttu-id="802c6-162">輸出</span><span class="sxs-lookup"><span data-stu-id="802c6-162">OUTPUTS</span></span>

### <span data-ttu-id="802c6-163">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="802c6-163">PSCustomObject.</span></span> <span data-ttu-id="802c6-164">在 PSCustomObject 中返回下列屬性</span><span class="sxs-lookup"><span data-stu-id="802c6-164">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="802c6-165">結果：成功或失敗或擱置ForAdminConsent或取消。</span><span class="sxs-lookup"><span data-stu-id="802c6-165">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="802c6-166">ResourceId：在 Azure 中建立之資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="802c6-166">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="802c6-167">PortalResourceURL：Azure 入口網站資源 URL。</span><span class="sxs-lookup"><span data-stu-id="802c6-167">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="802c6-168">PortalAADAppPermissionsURL：AAD App 許可權頁面的 Azure 入口網站 URL。</span><span class="sxs-lookup"><span data-stu-id="802c6-168">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="802c6-169">筆記</span><span class="sxs-lookup"><span data-stu-id="802c6-169">NOTES</span></span>

## <span data-ttu-id="802c6-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="802c6-170">RELATED LINKS</span></span>
