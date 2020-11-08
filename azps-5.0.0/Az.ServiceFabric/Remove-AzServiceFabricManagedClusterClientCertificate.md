---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: d9a3e5488fe55a1d5090fb21ffb211e6fcec53c2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137307"
---
# <span data-ttu-id="a7b7c-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="a7b7c-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="a7b7c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="a7b7c-103">依指紋或公用名 Remvoe 用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="a7b7c-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="a7b7c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7b7c-104">SYNTAX</span></span>

### <span data-ttu-id="a7b7c-105">ClientCertByTpByObj (預設) </span><span class="sxs-lookup"><span data-stu-id="a7b7c-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7b7c-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="a7b7c-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7b7c-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="a7b7c-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7b7c-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="a7b7c-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7b7c-109">說明</span><span class="sxs-lookup"><span data-stu-id="a7b7c-109">DESCRIPTION</span></span>
<span data-ttu-id="a7b7c-110">依指紋或公用名 Remvoe 用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="a7b7c-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="a7b7c-111">示例</span><span class="sxs-lookup"><span data-stu-id="a7b7c-111">EXAMPLES</span></span>

### <span data-ttu-id="a7b7c-112">範例1</span><span class="sxs-lookup"><span data-stu-id="a7b7c-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="a7b7c-113">依 [常用名稱] 移除用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="a7b7c-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="a7b7c-114">範例2</span><span class="sxs-lookup"><span data-stu-id="a7b7c-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="a7b7c-115">依指紋移除用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="a7b7c-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="a7b7c-116">範例3</span><span class="sxs-lookup"><span data-stu-id="a7b7c-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="a7b7c-117">以指紋移除用戶端憑證（含管道）。</span><span class="sxs-lookup"><span data-stu-id="a7b7c-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="a7b7c-118">參數</span><span class="sxs-lookup"><span data-stu-id="a7b7c-118">PARAMETERS</span></span>

### <span data-ttu-id="a7b7c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7b7c-119">-AsJob</span></span>
<span data-ttu-id="a7b7c-120">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="a7b7c-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a7b7c-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="a7b7c-121">-CommonName</span></span>
<span data-ttu-id="a7b7c-122">用戶端憑證公用名。</span><span class="sxs-lookup"><span data-stu-id="a7b7c-122">Client certificate common name.</span></span>

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

### <span data-ttu-id="a7b7c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7b7c-123">-DefaultProfile</span></span>
<span data-ttu-id="a7b7c-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7b7c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7b7c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7b7c-125">-InputObject</span></span>
<span data-ttu-id="a7b7c-126">受管理的群集資源</span><span class="sxs-lookup"><span data-stu-id="a7b7c-126">Managed cluster resource</span></span>

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

### <span data-ttu-id="a7b7c-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="a7b7c-127">-Name</span></span>
<span data-ttu-id="a7b7c-128">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7b7c-128">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7b7c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7b7c-129">-PassThru</span></span>
<span data-ttu-id="a7b7c-130">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="a7b7c-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="a7b7c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7b7c-131">-ResourceGroupName</span></span>
<span data-ttu-id="a7b7c-132">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7b7c-132">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByCnTpName, ClientCertByCnByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7b7c-133">-指紋</span><span class="sxs-lookup"><span data-stu-id="a7b7c-133">-Thumbprint</span></span>
<span data-ttu-id="a7b7c-134">用戶端憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="a7b7c-134">Client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientCertByTpByObj, ClientCertByCnTpName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7b7c-135">-確認</span><span class="sxs-lookup"><span data-stu-id="a7b7c-135">-Confirm</span></span>
<span data-ttu-id="a7b7c-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a7b7c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7b7c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7b7c-137">-WhatIf</span></span>
<span data-ttu-id="a7b7c-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a7b7c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7b7c-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7b7c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7b7c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7b7c-140">CommonParameters</span></span>
<span data-ttu-id="a7b7c-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a7b7c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7b7c-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a7b7c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7b7c-143">輸入</span><span class="sxs-lookup"><span data-stu-id="a7b7c-143">INPUTS</span></span>

### <span data-ttu-id="a7b7c-144">System.object</span><span class="sxs-lookup"><span data-stu-id="a7b7c-144">System.String</span></span>

## <span data-ttu-id="a7b7c-145">輸出</span><span class="sxs-lookup"><span data-stu-id="a7b7c-145">OUTPUTS</span></span>

### <span data-ttu-id="a7b7c-146">PSManagedCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="a7b7c-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="a7b7c-147">筆記</span><span class="sxs-lookup"><span data-stu-id="a7b7c-147">NOTES</span></span>

## <span data-ttu-id="a7b7c-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7b7c-148">RELATED LINKS</span></span>