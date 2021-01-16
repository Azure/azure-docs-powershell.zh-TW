---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: e948acb179a0ae6a338fa02f01d1cb7d6efbd4fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279967"
---
# <span data-ttu-id="a9094-101">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a9094-101">Add-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="a9094-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9094-102">SYNOPSIS</span></span>
<span data-ttu-id="a9094-103">在群集中新增證書公用名稱或指紋。</span><span class="sxs-lookup"><span data-stu-id="a9094-103">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="a9094-104">這會在群集中針對用戶端驗證註冊證書 agains。</span><span class="sxs-lookup"><span data-stu-id="a9094-104">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="a9094-105">句法</span><span class="sxs-lookup"><span data-stu-id="a9094-105">SYNTAX</span></span>

### <span data-ttu-id="a9094-106">ClientCertByTpByObj (預設) </span><span class="sxs-lookup"><span data-stu-id="a9094-106">ClientCertByTpByObj (Default)</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9094-107">ClientCertByTpByName</span><span class="sxs-lookup"><span data-stu-id="a9094-107">ClientCertByTpByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -Thumbprint <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9094-108">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="a9094-108">ClientCertByCnByName</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9094-109">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="a9094-109">ClientCertByCnByObj</span></span>
```
Add-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> [-Admin]
 -CommonName <String> [-IssuerThumbprint <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9094-110">說明</span><span class="sxs-lookup"><span data-stu-id="a9094-110">DESCRIPTION</span></span>
<span data-ttu-id="a9094-111">在群集中新增證書公用名稱或指紋。</span><span class="sxs-lookup"><span data-stu-id="a9094-111">Add certificate common name or thumbprint to the cluster.</span></span> <span data-ttu-id="a9094-112">這會在群集中針對用戶端驗證註冊證書 agains。</span><span class="sxs-lookup"><span data-stu-id="a9094-112">This will register the certificate agains the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="a9094-113">示例</span><span class="sxs-lookup"><span data-stu-id="a9094-113">EXAMPLES</span></span>

### <span data-ttu-id="a9094-114">範例1</span><span class="sxs-lookup"><span data-stu-id="a9094-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="a9094-115">這個命令會將指紋為「5F3660C715EBBDA31DB1FFDCF508302348DE8E7A」的憑證新增至群集，因此用戶端可以使用憑證作為系統管理員來與群集進行通訊。</span><span class="sxs-lookup"><span data-stu-id="a9094-115">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="a9094-116">範例2</span><span class="sxs-lookup"><span data-stu-id="a9094-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Add-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -ClusterName $clusterName -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="a9094-117">這個命令會新增具有公用名 ' Contoso.com」和2個頒發者的唯讀用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="a9094-117">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers.</span></span>

### <span data-ttu-id="a9094-118">範例3</span><span class="sxs-lookup"><span data-stu-id="a9094-118">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
$cluster | Add-AzServiceFabricManagedClusterClientCertificate -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, 5F3660C715EBBDA31DB1FFDCF508302348DE8E7B
```

<span data-ttu-id="a9094-119">這個命令會新增含有「Contoso.com」及2個 issuer （含管道）的唯讀用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="a9094-119">This command will add a read only client certificate with common name 'Contoso.com' and 2 issuers, with piping.</span></span>

## <span data-ttu-id="a9094-120">參數</span><span class="sxs-lookup"><span data-stu-id="a9094-120">PARAMETERS</span></span>

### <span data-ttu-id="a9094-121">-系統管理員</span><span class="sxs-lookup"><span data-stu-id="a9094-121">-Admin</span></span>
<span data-ttu-id="a9094-122">用來指定用戶端憑證是否擁有系統管理員層級。</span><span class="sxs-lookup"><span data-stu-id="a9094-122">Use to specify if the client certificate has administrator level.</span></span>

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

### <span data-ttu-id="a9094-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9094-123">-AsJob</span></span>
<span data-ttu-id="a9094-124">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="a9094-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a9094-125">-CommonName</span><span class="sxs-lookup"><span data-stu-id="a9094-125">-CommonName</span></span>
<span data-ttu-id="a9094-126">用戶端憑證公用名。</span><span class="sxs-lookup"><span data-stu-id="a9094-126">Client certificate common name.</span></span>

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

### <span data-ttu-id="a9094-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9094-127">-DefaultProfile</span></span>
<span data-ttu-id="a9094-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9094-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9094-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9094-129">-InputObject</span></span>
<span data-ttu-id="a9094-130">受管理的群集資源</span><span class="sxs-lookup"><span data-stu-id="a9094-130">Managed cluster resource</span></span>

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

### <span data-ttu-id="a9094-131">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="a9094-131">-IssuerThumbprint</span></span>
<span data-ttu-id="a9094-132">用戶端憑證的頒發者指紋清單。</span><span class="sxs-lookup"><span data-stu-id="a9094-132">List of Issuer thumbprints for the client certificate.</span></span>
<span data-ttu-id="a9094-133">僅搭配 CommonName 使用。</span><span class="sxs-lookup"><span data-stu-id="a9094-133">Only use in combination with CommonName.</span></span>

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

### <span data-ttu-id="a9094-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="a9094-134">-Name</span></span>
<span data-ttu-id="a9094-135">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9094-135">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a9094-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9094-136">-ResourceGroupName</span></span>
<span data-ttu-id="a9094-137">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9094-137">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a9094-138">-指紋</span><span class="sxs-lookup"><span data-stu-id="a9094-138">-Thumbprint</span></span>
<span data-ttu-id="a9094-139">用戶端憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="a9094-139">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="a9094-140">-確認</span><span class="sxs-lookup"><span data-stu-id="a9094-140">-Confirm</span></span>
<span data-ttu-id="a9094-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a9094-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9094-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9094-142">-WhatIf</span></span>
<span data-ttu-id="a9094-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a9094-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9094-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9094-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9094-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9094-145">CommonParameters</span></span>
<span data-ttu-id="a9094-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9094-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9094-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a9094-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9094-148">輸入</span><span class="sxs-lookup"><span data-stu-id="a9094-148">INPUTS</span></span>

### <span data-ttu-id="a9094-149">System.object</span><span class="sxs-lookup"><span data-stu-id="a9094-149">System.String</span></span>

## <span data-ttu-id="a9094-150">輸出</span><span class="sxs-lookup"><span data-stu-id="a9094-150">OUTPUTS</span></span>

### <span data-ttu-id="a9094-151">PSManagedCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="a9094-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="a9094-152">筆記</span><span class="sxs-lookup"><span data-stu-id="a9094-152">NOTES</span></span>

## <span data-ttu-id="a9094-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9094-153">RELATED LINKS</span></span>
