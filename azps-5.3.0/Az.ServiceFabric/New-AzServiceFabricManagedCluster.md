---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 9dd54f0f1ca56a8bedf3550e238a4308b519925d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448223"
---
# <span data-ttu-id="d227b-101">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="d227b-101">New-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="d227b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d227b-102">SYNOPSIS</span></span>
<span data-ttu-id="d227b-103">建立新的 managed 群集。</span><span class="sxs-lookup"><span data-stu-id="d227b-103">Create new managed cluster.</span></span>

## <span data-ttu-id="d227b-104">句法</span><span class="sxs-lookup"><span data-stu-id="d227b-104">SYNTAX</span></span>

### <span data-ttu-id="d227b-105">ClientCertByTp (預設) </span><span class="sxs-lookup"><span data-stu-id="d227b-105">ClientCertByTp (Default)</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertThumbprint <String> -AdminPassword <SecureString> [-AdminUserName <String>]
 [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>] [-DnsName <String>]
 [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d227b-106">ClientCertByCn</span><span class="sxs-lookup"><span data-stu-id="d227b-106">ClientCertByCn</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertCommonName <String> [-ClientCertIssuerThumbprint <String[]>] -AdminPassword <SecureString>
 [-AdminUserName <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d227b-107">說明</span><span class="sxs-lookup"><span data-stu-id="d227b-107">DESCRIPTION</span></span>
<span data-ttu-id="d227b-108">這個 Cmdlet 會建立不含節點類型的受管理的群集資源。</span><span class="sxs-lookup"><span data-stu-id="d227b-108">This cmdlet will create a managed cluster resource without node types.</span></span> <span data-ttu-id="d227b-109">若要引導群集，需要新增主要節點類型使用 [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md)。</span><span class="sxs-lookup"><span data-stu-id="d227b-109">To bootstrap the cluster A primary node type needs to be added use [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span></span>

## <span data-ttu-id="d227b-110">示例</span><span class="sxs-lookup"><span data-stu-id="d227b-110">EXAMPLES</span></span>

### <span data-ttu-id="d227b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d227b-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -AdminPassword $password -Verbose
```

<span data-ttu-id="d227b-112">這個命令會建立含預設基本 sku 的群集資源。</span><span class="sxs-lookup"><span data-stu-id="d227b-112">This command creates a cluster resource with default basic sku.</span></span>

### <span data-ttu-id="d227b-113">範例2</span><span class="sxs-lookup"><span data-stu-id="d227b-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -ClientCertThumbprint XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX -ClientCertIsAdmin -AdminPassword $password -Sku Standard -Verbose
```

<span data-ttu-id="d227b-114">這個命令會在 centraluseuap 中使用初始系統管理員用戶端憑證和標準 sku 來建立群集資源。</span><span class="sxs-lookup"><span data-stu-id="d227b-114">This command creates a cluster resource in centraluseuap with an initial admin client certificate and standard sku.</span></span>

## <span data-ttu-id="d227b-115">參數</span><span class="sxs-lookup"><span data-stu-id="d227b-115">PARAMETERS</span></span>

### <span data-ttu-id="d227b-116">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="d227b-116">-AdminPassword</span></span>
<span data-ttu-id="d227b-117">虛擬機器使用的系統管理密碼。</span><span class="sxs-lookup"><span data-stu-id="d227b-117">Admin password used for the virtual machines.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d227b-118">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="d227b-118">-AdminUserName</span></span>
<span data-ttu-id="d227b-119">虛擬機器使用的系統管理密碼。</span><span class="sxs-lookup"><span data-stu-id="d227b-119">Admin password used for the virtual machines.</span></span>
<span data-ttu-id="d227b-120">預設值： vmadmin。</span><span class="sxs-lookup"><span data-stu-id="d227b-120">Default: vmadmin.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "vmadmin"
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d227b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d227b-121">-AsJob</span></span>
<span data-ttu-id="d227b-122">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="d227b-122">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d227b-123">-ClientCertCommonName</span><span class="sxs-lookup"><span data-stu-id="d227b-123">-ClientCertCommonName</span></span>
<span data-ttu-id="d227b-124">用戶端憑證公用名。</span><span class="sxs-lookup"><span data-stu-id="d227b-124">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d227b-125">-ClientCertIsAdmin</span><span class="sxs-lookup"><span data-stu-id="d227b-125">-ClientCertIsAdmin</span></span>
<span data-ttu-id="d227b-126">用來指定用戶端憑證是否擁有系統管理員層級。</span><span class="sxs-lookup"><span data-stu-id="d227b-126">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="d227b-127">-ClientCertIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="d227b-127">-ClientCertIssuerThumbprint</span></span>
<span data-ttu-id="d227b-128">用戶端憑證的頒發者指紋清單。</span><span class="sxs-lookup"><span data-stu-id="d227b-128">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="d227b-129">僅搭配 ClientCertCommonName 使用。</span><span class="sxs-lookup"><span data-stu-id="d227b-129">Only use in combination with ClientCertCommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d227b-130">-ClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="d227b-130">-ClientCertThumbprint</span></span>
<span data-ttu-id="d227b-131">用戶端憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="d227b-131">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d227b-132">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="d227b-132">-ClientConnectionPort</span></span>
<span data-ttu-id="d227b-133">用於用戶端連線至群集的埠。</span><span class="sxs-lookup"><span data-stu-id="d227b-133">Port used for client connections to the cluster.</span></span>
<span data-ttu-id="d227b-134">預設：19000。</span><span class="sxs-lookup"><span data-stu-id="d227b-134">Default: 19000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 19000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d227b-135">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="d227b-135">-CodeVersion</span></span>
<span data-ttu-id="d227b-136">叢集服務結構程式碼版本。</span><span class="sxs-lookup"><span data-stu-id="d227b-136">Cluster service fabric code version.</span></span>
<span data-ttu-id="d227b-137">只有在 [升級模式] 為 [手動] 時才使用。</span><span class="sxs-lookup"><span data-stu-id="d227b-137">Only use if upgrade mode is Manual.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d227b-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d227b-138">-DefaultProfile</span></span>
<span data-ttu-id="d227b-139">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d227b-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d227b-140">-DnsName</span><span class="sxs-lookup"><span data-stu-id="d227b-140">-DnsName</span></span>
<span data-ttu-id="d227b-141">群集的 dns 名稱。</span><span class="sxs-lookup"><span data-stu-id="d227b-141">Cluster's dns name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d227b-142">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="d227b-142">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="d227b-143">用於連接至群集的 HTTP 連線埠。</span><span class="sxs-lookup"><span data-stu-id="d227b-143">Port used for http connections to the cluster.</span></span>
<span data-ttu-id="d227b-144">預設：19080。</span><span class="sxs-lookup"><span data-stu-id="d227b-144">Default: 19080.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 19080
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d227b-145">-位置</span><span class="sxs-lookup"><span data-stu-id="d227b-145">-Location</span></span>
<span data-ttu-id="d227b-146">資源位置</span><span class="sxs-lookup"><span data-stu-id="d227b-146">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d227b-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="d227b-147">-Name</span></span>
<span data-ttu-id="d227b-148">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="d227b-148">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d227b-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d227b-149">-ResourceGroupName</span></span>
<span data-ttu-id="d227b-150">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d227b-150">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d227b-151">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="d227b-151">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="d227b-152">反向 proxy 使用的端點。</span><span class="sxs-lookup"><span data-stu-id="d227b-152">Endpoint used by reverse proxy.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d227b-153">-Sku</span><span class="sxs-lookup"><span data-stu-id="d227b-153">-Sku</span></span>
<span data-ttu-id="d227b-154">群集的 Sku，選項為基本：它至少會有3個種子節點，且只允許1個節點類型及標準：它至少有5種子節點，且允許多個節點類型。</span><span class="sxs-lookup"><span data-stu-id="d227b-154">Cluster's Sku, the options are Basic: it will have a minimum of 3 seed nodes and only allows 1 node type and Standard: it will have a minimum of 5 seed nodes and allows multiple node types.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ManagedClusterSku
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard

Required: False
Position: Named
Default value: Basic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d227b-155">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="d227b-155">-UpgradeMode</span></span>
<span data-ttu-id="d227b-156">叢集服務結構程式碼版本升級模式。</span><span class="sxs-lookup"><span data-stu-id="d227b-156">Cluster service fabric code version upgrade mode.</span></span>
<span data-ttu-id="d227b-157">[自動] 或 [手動]。</span><span class="sxs-lookup"><span data-stu-id="d227b-157">Automatic or Manual.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d227b-158">-UseTestExtension</span><span class="sxs-lookup"><span data-stu-id="d227b-158">-UseTestExtension</span></span>
<span data-ttu-id="d227b-159">如果指定 [群集]，將會 crated 服務測試 vmss 延伸。</span><span class="sxs-lookup"><span data-stu-id="d227b-159">If Specify The cluster will be crated with service test vmss extension.</span></span>

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

### <span data-ttu-id="d227b-160">-確認</span><span class="sxs-lookup"><span data-stu-id="d227b-160">-Confirm</span></span>
<span data-ttu-id="d227b-161">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d227b-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d227b-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d227b-162">-WhatIf</span></span>
<span data-ttu-id="d227b-163">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d227b-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d227b-164">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d227b-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d227b-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d227b-165">CommonParameters</span></span>
<span data-ttu-id="d227b-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d227b-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d227b-167">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d227b-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d227b-168">輸入</span><span class="sxs-lookup"><span data-stu-id="d227b-168">INPUTS</span></span>

### <span data-ttu-id="d227b-169">System.object</span><span class="sxs-lookup"><span data-stu-id="d227b-169">System.String</span></span>

## <span data-ttu-id="d227b-170">輸出</span><span class="sxs-lookup"><span data-stu-id="d227b-170">OUTPUTS</span></span>

### <span data-ttu-id="d227b-171">PSManagedCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="d227b-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="d227b-172">筆記</span><span class="sxs-lookup"><span data-stu-id="d227b-172">NOTES</span></span>

## <span data-ttu-id="d227b-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="d227b-173">RELATED LINKS</span></span>

[<span data-ttu-id="d227b-174">新-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="d227b-174">New-AzServiceFabricManagedNodeType</span></span>](./New-AzServiceFabricManagedNodeType.md)