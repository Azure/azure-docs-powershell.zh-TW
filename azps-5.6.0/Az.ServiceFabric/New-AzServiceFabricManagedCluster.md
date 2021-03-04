---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricManagedCluster.md
ms.openlocfilehash: b6f948de5c5e1eea666086b839d314ace6394e98
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906498"
---
# <span data-ttu-id="63fb6-101">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="63fb6-101">New-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="63fb6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="63fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="63fb6-103">建立新受管理的集區。</span><span class="sxs-lookup"><span data-stu-id="63fb6-103">Create new managed cluster.</span></span>

## <span data-ttu-id="63fb6-104">語法</span><span class="sxs-lookup"><span data-stu-id="63fb6-104">SYNTAX</span></span>

### <span data-ttu-id="63fb6-105">ClientCertByTp (預設) </span><span class="sxs-lookup"><span data-stu-id="63fb6-105">ClientCertByTp (Default)</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertThumbprint <String> -AdminPassword <SecureString> [-AdminUserName <String>]
 [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>] [-DnsName <String>]
 [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63fb6-106">ClientCertByCn</span><span class="sxs-lookup"><span data-stu-id="63fb6-106">ClientCertByCn</span></span>
```
New-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-ClientCertIsAdmin]
 -ClientCertCommonName <String> [-ClientCertIssuerThumbprint <String[]>] -AdminPassword <SecureString>
 [-AdminUserName <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-Sku <ManagedClusterSku>] [-UseTestExtension]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63fb6-107">描述</span><span class="sxs-lookup"><span data-stu-id="63fb6-107">DESCRIPTION</span></span>
<span data-ttu-id="63fb6-108">此 Cmdlet 會建立不含節點類型的受管理的組群資源。</span><span class="sxs-lookup"><span data-stu-id="63fb6-108">This cmdlet will create a managed cluster resource without node types.</span></span> <span data-ttu-id="63fb6-109">若要啟動該組集，必須新增主要節點類型[New-AzServiceFabricManagedNodeType。](./New-AzServiceFabricManagedNodeType.md)</span><span class="sxs-lookup"><span data-stu-id="63fb6-109">To bootstrap the cluster A primary node type needs to be added use [New-AzServiceFabricManagedNodeType](./New-AzServiceFabricManagedNodeType.md).</span></span>

## <span data-ttu-id="63fb6-110">例子</span><span class="sxs-lookup"><span data-stu-id="63fb6-110">EXAMPLES</span></span>

### <span data-ttu-id="63fb6-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="63fb6-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -AdminPassword $password -Verbose
```

<span data-ttu-id="63fb6-112">此命令會建立具有預設基本 SKU 的集區資源。</span><span class="sxs-lookup"><span data-stu-id="63fb6-112">This command creates a cluster resource with default basic sku.</span></span>

### <span data-ttu-id="63fb6-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="63fb6-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$password = ConvertTo-SecureString -AsPlainText -Force "testpass1234!@#$"
New-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Location centraluseuap -ClusterName $clusterName -ClientCertThumbprint XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX -ClientCertIsAdmin -AdminPassword $password -Sku Standard -Verbose
```

<span data-ttu-id="63fb6-114">此命令會使用初始系統管理員用戶端憑證和標準 SKU 在 centraluseuap 中建立一個集區資源。</span><span class="sxs-lookup"><span data-stu-id="63fb6-114">This command creates a cluster resource in centraluseuap with an initial admin client certificate and standard sku.</span></span>

## <span data-ttu-id="63fb6-115">參數</span><span class="sxs-lookup"><span data-stu-id="63fb6-115">PARAMETERS</span></span>

### <span data-ttu-id="63fb6-116">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="63fb6-116">-AdminPassword</span></span>
<span data-ttu-id="63fb6-117">用於虛擬機器的系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="63fb6-117">Admin password used for the virtual machines.</span></span>

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

### <span data-ttu-id="63fb6-118">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="63fb6-118">-AdminUserName</span></span>
<span data-ttu-id="63fb6-119">用於虛擬機器的系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="63fb6-119">Admin password used for the virtual machines.</span></span>
<span data-ttu-id="63fb6-120">預設值：vmadmin。</span><span class="sxs-lookup"><span data-stu-id="63fb6-120">Default: vmadmin.</span></span>

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

### <span data-ttu-id="63fb6-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63fb6-121">-AsJob</span></span>
<span data-ttu-id="63fb6-122">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="63fb6-122">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="63fb6-123">-ClientCertCommonName</span><span class="sxs-lookup"><span data-stu-id="63fb6-123">-ClientCertCommonName</span></span>
<span data-ttu-id="63fb6-124">用戶端憑證通用名稱。</span><span class="sxs-lookup"><span data-stu-id="63fb6-124">Client certificate common name.</span></span>

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

### <span data-ttu-id="63fb6-125">-ClientCertIsAdmin</span><span class="sxs-lookup"><span data-stu-id="63fb6-125">-ClientCertIsAdmin</span></span>
<span data-ttu-id="63fb6-126">用於指定用戶端憑證是否具有系統管理員層級。</span><span class="sxs-lookup"><span data-stu-id="63fb6-126">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="63fb6-127">-ClientCertIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="63fb6-127">-ClientCertIssuerThumbprint</span></span>
<span data-ttu-id="63fb6-128">用戶端憑證的發行者指紋清單。</span><span class="sxs-lookup"><span data-stu-id="63fb6-128">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="63fb6-129">只能與 ClientCertCommonName 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="63fb6-129">Only use in combination with ClientCertCommonName.</span></span>

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

### <span data-ttu-id="63fb6-130">-ClientCertThumbprint</span><span class="sxs-lookup"><span data-stu-id="63fb6-130">-ClientCertThumbprint</span></span>
<span data-ttu-id="63fb6-131">用戶端憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="63fb6-131">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="63fb6-132">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="63fb6-132">-ClientConnectionPort</span></span>
<span data-ttu-id="63fb6-133">用於用戶端連接到該組集的埠。</span><span class="sxs-lookup"><span data-stu-id="63fb6-133">Port used for client connections to the cluster.</span></span>
<span data-ttu-id="63fb6-134">預設值：19000。</span><span class="sxs-lookup"><span data-stu-id="63fb6-134">Default: 19000.</span></span>

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

### <span data-ttu-id="63fb6-135">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="63fb6-135">-CodeVersion</span></span>
<span data-ttu-id="63fb6-136">集區服務結構代碼版本。</span><span class="sxs-lookup"><span data-stu-id="63fb6-136">Cluster service fabric code version.</span></span>
<span data-ttu-id="63fb6-137">只有在升級模式為手動時才能使用。</span><span class="sxs-lookup"><span data-stu-id="63fb6-137">Only use if upgrade mode is Manual.</span></span>

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

### <span data-ttu-id="63fb6-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63fb6-138">-DefaultProfile</span></span>
<span data-ttu-id="63fb6-139">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="63fb6-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63fb6-140">-DnsName</span><span class="sxs-lookup"><span data-stu-id="63fb6-140">-DnsName</span></span>
<span data-ttu-id="63fb6-141">Cluster 的 dns 名稱。</span><span class="sxs-lookup"><span data-stu-id="63fb6-141">Cluster's dns name.</span></span>

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

### <span data-ttu-id="63fb6-142">-HTTPGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="63fb6-142">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="63fb6-143">用於將 HTTP 連結至該組集的埠。</span><span class="sxs-lookup"><span data-stu-id="63fb6-143">Port used for http connections to the cluster.</span></span>
<span data-ttu-id="63fb6-144">預設值：19080。</span><span class="sxs-lookup"><span data-stu-id="63fb6-144">Default: 19080.</span></span>

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

### <span data-ttu-id="63fb6-145">-位置</span><span class="sxs-lookup"><span data-stu-id="63fb6-145">-Location</span></span>
<span data-ttu-id="63fb6-146">資源位置</span><span class="sxs-lookup"><span data-stu-id="63fb6-146">The resource location</span></span>

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

### <span data-ttu-id="63fb6-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="63fb6-147">-Name</span></span>
<span data-ttu-id="63fb6-148">指定組名。</span><span class="sxs-lookup"><span data-stu-id="63fb6-148">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="63fb6-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63fb6-149">-ResourceGroupName</span></span>
<span data-ttu-id="63fb6-150">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="63fb6-150">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="63fb6-151">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="63fb6-151">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="63fb6-152">由反向 Proxy 使用的端點。</span><span class="sxs-lookup"><span data-stu-id="63fb6-152">Endpoint used by reverse proxy.</span></span>

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

### <span data-ttu-id="63fb6-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="63fb6-153">-Sku</span></span>
<span data-ttu-id="63fb6-154">Cluster 的 SKU 選項為基本：它會有至少 3 個子節點，並且只允許 1 個節點類型和標準：它至少具有 5 個子節點，並允許多個節點類型。</span><span class="sxs-lookup"><span data-stu-id="63fb6-154">Cluster's Sku, the options are Basic: it will have a minimum of 3 seed nodes and only allows 1 node type and Standard: it will have a minimum of 5 seed nodes and allows multiple node types.</span></span>

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

### <span data-ttu-id="63fb6-155">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="63fb6-155">-UpgradeMode</span></span>
<span data-ttu-id="63fb6-156">集區服務結構代碼版本升級模式。</span><span class="sxs-lookup"><span data-stu-id="63fb6-156">Cluster service fabric code version upgrade mode.</span></span>
<span data-ttu-id="63fb6-157">自動或手動。</span><span class="sxs-lookup"><span data-stu-id="63fb6-157">Automatic or Manual.</span></span>

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

### <span data-ttu-id="63fb6-158">-UseTestExtension</span><span class="sxs-lookup"><span data-stu-id="63fb6-158">-UseTestExtension</span></span>
<span data-ttu-id="63fb6-159">如果指定該組組會以服務測試 vms 副檔名進行分級。</span><span class="sxs-lookup"><span data-stu-id="63fb6-159">If Specify The cluster will be crated with service test vmss extension.</span></span>

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

### <span data-ttu-id="63fb6-160">-確認</span><span class="sxs-lookup"><span data-stu-id="63fb6-160">-Confirm</span></span>
<span data-ttu-id="63fb6-161">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="63fb6-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63fb6-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63fb6-162">-WhatIf</span></span>
<span data-ttu-id="63fb6-163">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="63fb6-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63fb6-164">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="63fb6-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63fb6-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63fb6-165">CommonParameters</span></span>
<span data-ttu-id="63fb6-166">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="63fb6-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63fb6-167">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63fb6-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63fb6-168">輸入</span><span class="sxs-lookup"><span data-stu-id="63fb6-168">INPUTS</span></span>

### <span data-ttu-id="63fb6-169">System.String</span><span class="sxs-lookup"><span data-stu-id="63fb6-169">System.String</span></span>

## <span data-ttu-id="63fb6-170">輸出</span><span class="sxs-lookup"><span data-stu-id="63fb6-170">OUTPUTS</span></span>

### <span data-ttu-id="63fb6-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="63fb6-171">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="63fb6-172">筆記</span><span class="sxs-lookup"><span data-stu-id="63fb6-172">NOTES</span></span>

## <span data-ttu-id="63fb6-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="63fb6-173">RELATED LINKS</span></span>

[<span data-ttu-id="63fb6-174">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="63fb6-174">New-AzServiceFabricManagedNodeType</span></span>](./New-AzServiceFabricManagedNodeType.md)