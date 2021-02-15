---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: a96ca28b750628eef1b0395e5867bb7f7341fba0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130619"
---
# <span data-ttu-id="1385e-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="1385e-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="1385e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1385e-102">SYNOPSIS</span></span>
<span data-ttu-id="1385e-103">Register-AzStackHCI 會建立代表內部部署群集的 AzureStackHCI 雲端資源，並使用 Azure 註冊內部部署的群集。</span><span class="sxs-lookup"><span data-stu-id="1385e-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="1385e-104">句法</span><span class="sxs-lookup"><span data-stu-id="1385e-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-CertificateThumbprint] <String>] [-RepairRegistration]
 [-UseDeviceAuthentication] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="1385e-105">說明</span><span class="sxs-lookup"><span data-stu-id="1385e-105">DESCRIPTION</span></span>
<span data-ttu-id="1385e-106">Register-AzStackHCI 會建立代表內部部署群集的 AzureStackHCI 雲端資源，並使用 Azure 註冊內部部署的群集。</span><span class="sxs-lookup"><span data-stu-id="1385e-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="1385e-107">示例</span><span class="sxs-lookup"><span data-stu-id="1385e-107">EXAMPLES</span></span>

### <span data-ttu-id="1385e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1385e-108">EXAMPLE 1</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" 
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/
```

<span data-ttu-id="1385e-109">在其中一個叢集節點上喚醒。</span><span class="sxs-lookup"><span data-stu-id="1385e-109">Invoking on one of the cluster node.</span></span>

### <span data-ttu-id="1385e-110">範例2</span><span class="sxs-lookup"><span data-stu-id="1385e-110">EXAMPLE 2</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="1385e-111">從管理節點進行喚醒。</span><span class="sxs-lookup"><span data-stu-id="1385e-111">Invoking from the management node.</span></span>

### <span data-ttu-id="1385e-112">範例3</span><span class="sxs-lookup"><span data-stu-id="1385e-112">EXAMPLE 3</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG 
Result: PendingForAdminConsent
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="1385e-113">從 WAC 進行喚醒。</span><span class="sxs-lookup"><span data-stu-id="1385e-113">Invoking from WAC.</span></span>

### <span data-ttu-id="1385e-114">範例4</span><span class="sxs-lookup"><span data-stu-id="1385e-114">EXAMPLE 4</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="1385e-115">使用所有參數進行喚醒。</span><span class="sxs-lookup"><span data-stu-id="1385e-115">Invoking with all the parameters.</span></span>

## <span data-ttu-id="1385e-116">參數</span><span class="sxs-lookup"><span data-stu-id="1385e-116">PARAMETERS</span></span>

### <span data-ttu-id="1385e-117">-AccountId</span><span class="sxs-lookup"><span data-stu-id="1385e-117">-AccountId</span></span>
<span data-ttu-id="1385e-118">指定 ARM 存取權杖。</span><span class="sxs-lookup"><span data-stu-id="1385e-118">Specifies the ARM access token.</span></span>
<span data-ttu-id="1385e-119">將它與 ArmAccessToken 和 GraphAccessToken 一起指定，將會避開 Azure 互動式登入。</span><span class="sxs-lookup"><span data-stu-id="1385e-119">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="1385e-120">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="1385e-120">-ArmAccessToken</span></span>
<span data-ttu-id="1385e-121">指定 ARM 存取權杖。</span><span class="sxs-lookup"><span data-stu-id="1385e-121">Specifies the ARM access token.</span></span>
<span data-ttu-id="1385e-122">將此指定與 GraphAccessToken 和 AccountId 搭配使用，就可以避免 Azure 互動式登入。</span><span class="sxs-lookup"><span data-stu-id="1385e-122">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="1385e-123">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="1385e-123">-CertificateThumbprint</span></span>
<span data-ttu-id="1385e-124">指定所有節點上可用的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="1385e-124">Specifies the thumbprint of the certificate available on all the nodes.</span></span> <span data-ttu-id="1385e-125">使用者負責管理憑證。</span><span class="sxs-lookup"><span data-stu-id="1385e-125">User is responsible for managing the certificate.</span></span>

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

### <span data-ttu-id="1385e-126">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="1385e-126">-ComputerName</span></span>
<span data-ttu-id="1385e-127">指定群集名稱或內部部署群集中要註冊至 Azure 的叢集節點之一。</span><span class="sxs-lookup"><span data-stu-id="1385e-127">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="1385e-128">-認證</span><span class="sxs-lookup"><span data-stu-id="1385e-128">-Credential</span></span>
<span data-ttu-id="1385e-129">指定 ComputerName 的認證。</span><span class="sxs-lookup"><span data-stu-id="1385e-129">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="1385e-130">[預設值] 是執行 Cmdlet 的目前使用者。</span><span class="sxs-lookup"><span data-stu-id="1385e-130">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="1385e-131">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="1385e-131">-EnvironmentName</span></span>
<span data-ttu-id="1385e-132">指定 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="1385e-132">Specifies the Azure Environment.</span></span>
<span data-ttu-id="1385e-133">預設值為 AzureCloud。</span><span class="sxs-lookup"><span data-stu-id="1385e-133">Default is AzureCloud.</span></span>
<span data-ttu-id="1385e-134">有效值為 AzureCloud、AzureChinaCloud、AzureUSGovernment、AzureGermanCloud、AzurePPE</span><span class="sxs-lookup"><span data-stu-id="1385e-134">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="1385e-135">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="1385e-135">-GraphAccessToken</span></span>
<span data-ttu-id="1385e-136">指定圖形存取權杖。</span><span class="sxs-lookup"><span data-stu-id="1385e-136">Specifies the Graph access token.</span></span>
<span data-ttu-id="1385e-137">將此指定與 ArmAccessToken 和 AccountId 搭配使用，就可以避免 Azure 互動式登入。</span><span class="sxs-lookup"><span data-stu-id="1385e-137">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="1385e-138">-Region</span><span class="sxs-lookup"><span data-stu-id="1385e-138">-Region</span></span>
<span data-ttu-id="1385e-139">指定要建立資源的區域。</span><span class="sxs-lookup"><span data-stu-id="1385e-139">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="1385e-140">預設值為 EastUS。</span><span class="sxs-lookup"><span data-stu-id="1385e-140">Default is EastUS.</span></span>

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

### <span data-ttu-id="1385e-141">-RepairRegistration</span><span class="sxs-lookup"><span data-stu-id="1385e-141">-RepairRegistration</span></span>
<span data-ttu-id="1385e-142">使用雲端修復目前的 Azure 堆疊 HCI 註冊。</span><span class="sxs-lookup"><span data-stu-id="1385e-142">Repair the current Azure Stack HCI registration with the cloud.</span></span> <span data-ttu-id="1385e-143">這個 Cmdlet 會刪除叢集節點上的本機憑證以及雲端 Azure AD 應用程式中的遠端憑證，並為這兩者產生新的替換憑證。</span><span class="sxs-lookup"><span data-stu-id="1385e-143">This cmdlet deletes the local certificates on the clustered nodes and the remote certificates in the Azure AD application in the cloud and generates new replacement certificates for both.</span></span> <span data-ttu-id="1385e-144">資源群組、資源名稱及其他註冊選項都會保留。</span><span class="sxs-lookup"><span data-stu-id="1385e-144">The resource group, resource name, and other registration choices are preserved.</span></span>

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

### <span data-ttu-id="1385e-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1385e-145">-ResourceGroupName</span></span>
<span data-ttu-id="1385e-146">指定 Azure 資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1385e-146">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="1385e-147">如果沒有指定 \<LocalClusterName\> ，則會將 rg 用作資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1385e-147">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="1385e-148">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="1385e-148">-ResourceName</span></span>
<span data-ttu-id="1385e-149">指定在 Azure 中建立之資源的資源名稱。</span><span class="sxs-lookup"><span data-stu-id="1385e-149">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="1385e-150">如果沒有指定，則會使用內部部署的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="1385e-150">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="1385e-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1385e-151">-SubscriptionId</span></span>
<span data-ttu-id="1385e-152">指定要建立資源的 Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="1385e-152">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="1385e-153">這是唯一的強制參數。</span><span class="sxs-lookup"><span data-stu-id="1385e-153">This is the only Mandatory parameter.</span></span>

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

### <span data-ttu-id="1385e-154">-TenantId</span><span class="sxs-lookup"><span data-stu-id="1385e-154">-TenantId</span></span>
<span data-ttu-id="1385e-155">指定 Azure TenantId。</span><span class="sxs-lookup"><span data-stu-id="1385e-155">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="1385e-156">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="1385e-156">-UseDeviceAuthentication</span></span>
<span data-ttu-id="1385e-157">使用裝置程式碼驗證，而非互動式瀏覽器提示。</span><span class="sxs-lookup"><span data-stu-id="1385e-157">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="1385e-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1385e-158">CommonParameters</span></span>
<span data-ttu-id="1385e-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1385e-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1385e-160">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1385e-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1385e-161">輸入</span><span class="sxs-lookup"><span data-stu-id="1385e-161">INPUTS</span></span>

## <span data-ttu-id="1385e-162">輸出</span><span class="sxs-lookup"><span data-stu-id="1385e-162">OUTPUTS</span></span>

### <span data-ttu-id="1385e-163">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="1385e-163">PSCustomObject.</span></span> <span data-ttu-id="1385e-164">在 PSCustomObject 中傳回下列屬性</span><span class="sxs-lookup"><span data-stu-id="1385e-164">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="1385e-165">結果：成功或失敗，或 PendingForAdminConsent 或取消。</span><span class="sxs-lookup"><span data-stu-id="1385e-165">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="1385e-166">ResourceId：在 Azure 中建立之資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1385e-166">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="1385e-167">PortalResourceURL： Azure 入口網站資源 URL。</span><span class="sxs-lookup"><span data-stu-id="1385e-167">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="1385e-168">PortalAADAppPermissionsURL： AAD App 許可權頁面的 Azure 入口網站 URL。</span><span class="sxs-lookup"><span data-stu-id="1385e-168">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="1385e-169">筆記</span><span class="sxs-lookup"><span data-stu-id="1385e-169">NOTES</span></span>

## <span data-ttu-id="1385e-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="1385e-170">RELATED LINKS</span></span>
