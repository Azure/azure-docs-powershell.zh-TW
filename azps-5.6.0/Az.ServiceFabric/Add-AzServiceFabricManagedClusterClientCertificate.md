---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: 11534ff7102295cd312410c5ecbae932fd9459e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906382"
---
# <span data-ttu-id="69907-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="69907-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="69907-102">簡介</span><span class="sxs-lookup"><span data-stu-id="69907-102">SYNOPSIS</span></span>
<span data-ttu-id="69907-103">在組塊中新增憑證通用名稱或指紋。</span><span class="sxs-lookup"><span data-stu-id="69907-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="69907-104">這將會再次註冊憑證，以用於用戶端驗證目的。</span><span class="sxs-lookup"><span data-stu-id="69907-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="69907-105">語法</span><span class="sxs-lookup"><span data-stu-id="69907-105">SYNTAX</span></span>

### <span data-ttu-id="69907-106">ClientCertByTpByObj (預設) </span><span class="sxs-lookup"><span data-stu-id="69907-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69907-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="69907-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69907-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="69907-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69907-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="69907-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69907-110">描述</span><span class="sxs-lookup"><span data-stu-id="69907-110">DESCRIPTION</span></span>
<span data-ttu-id="69907-111">在組塊中新增憑證通用名稱或指紋。</span><span class="sxs-lookup"><span data-stu-id="69907-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="69907-112">這將會再次註冊憑證，以用於用戶端驗證目的。</span><span class="sxs-lookup"><span data-stu-id="69907-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="69907-113">例子</span><span class="sxs-lookup"><span data-stu-id="69907-113">EXAMPLES</span></span>

### <span data-ttu-id="69907-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="69907-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="69907-115">此命令會使用指紋 '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A'新增憑證至該組，因此用戶端可以使用憑證做為系統管理員，與組塊通訊。</span><span class="sxs-lookup"><span data-stu-id="69907-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="69907-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="69907-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="69907-117">此命令會新增一個唯讀的用戶端憑證，並包含共同名稱 "Contoso.com" 和 2 個發行者。</span><span class="sxs-lookup"><span data-stu-id="69907-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="69907-118">範例 3</span><span class="sxs-lookup"><span data-stu-id="69907-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="69907-119">此命令會新增一個唯讀的用戶端憑證，並包含共同名稱 "Contoso.com" 和 2 個發行者，並且有管道。</span><span class="sxs-lookup"><span data-stu-id="69907-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="69907-120">參數</span><span class="sxs-lookup"><span data-stu-id="69907-120">PARAMETERS</span></span>

### <span data-ttu-id="69907-121">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="69907-121">-Admin</span></span>
<span data-ttu-id="69907-122">用於指定用戶端憑證是否具有系統管理員層級。</span><span class="sxs-lookup"><span data-stu-id="69907-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="69907-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69907-123">-AsJob</span></span>
<span data-ttu-id="69907-124">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="69907-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="69907-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="69907-125">-CommonName</span></span>
<span data-ttu-id="69907-126">用戶端憑證通用名稱。</span><span class="sxs-lookup"><span data-stu-id="69907-126">Client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69907-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69907-127">-DefaultProfile</span></span>
<span data-ttu-id="69907-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="69907-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69907-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69907-129">-InputObject</span></span>
<span data-ttu-id="69907-130">受管理的組群資源</span><span class="sxs-lookup"><span data-stu-id="69907-130">Managed cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ClientCertByTpByObj, ClientCertByCnByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69907-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="69907-131">-IssuerThumbprint</span></span>
<span data-ttu-id="69907-132">用戶端憑證的發行者指紋清單。</span><span class="sxs-lookup"><span data-stu-id="69907-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="69907-133">只能與 CommonName 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="69907-133">Only use in combination with CommonName.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ClientCertByCnByName, ClientCertByCnByObj
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69907-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="69907-134">-Name</span></span>
<span data-ttu-id="69907-135">指定組名。</span><span class="sxs-lookup"><span data-stu-id="69907-135">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69907-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69907-136">-ResourceGroupName</span></span>
<span data-ttu-id="69907-137">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="69907-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69907-138">-拇指列印</span><span class="sxs-lookup"><span data-stu-id="69907-138">-Thumbprint</span></span>
<span data-ttu-id="69907-139">用戶端憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="69907-139">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByTpByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69907-140">-確認</span><span class="sxs-lookup"><span data-stu-id="69907-140">-Confirm</span></span>
<span data-ttu-id="69907-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="69907-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69907-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69907-142">-WhatIf</span></span>
<span data-ttu-id="69907-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="69907-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69907-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69907-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69907-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69907-145">CommonParameters</span></span>
<span data-ttu-id="69907-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="69907-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69907-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69907-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69907-148">輸入</span><span class="sxs-lookup"><span data-stu-id="69907-148">INPUTS</span></span>

### <span data-ttu-id="69907-149">System.String</span><span class="sxs-lookup"><span data-stu-id="69907-149">System.String</span></span>

## <span data-ttu-id="69907-150">輸出</span><span class="sxs-lookup"><span data-stu-id="69907-150">OUTPUTS</span></span>

### <span data-ttu-id="69907-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="69907-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="69907-152">筆記</span><span class="sxs-lookup"><span data-stu-id="69907-152">NOTES</span></span>

## <span data-ttu-id="69907-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="69907-153">RELATED LINKS</span></span>
