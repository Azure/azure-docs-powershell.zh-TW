---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricmanagedclusterclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedClusterClientCertificate.md
ms.openlocfilehash: f0ba5cb4d461bbc70ba742ae46ba4b9489923545
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915825"
---
# <span data-ttu-id="510af-101">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="510af-101">Remove-AzServiceFabricManagedClusterClientCertificate</span></span>

## <span data-ttu-id="510af-102">簡介</span><span class="sxs-lookup"><span data-stu-id="510af-102">SYNOPSIS</span></span>
<span data-ttu-id="510af-103">以指紋或通用名稱重新叫用用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="510af-103">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="510af-104">語法</span><span class="sxs-lookup"><span data-stu-id="510af-104">SYNTAX</span></span>

### <span data-ttu-id="510af-105">ClientCertByTpByObj (預設) </span><span class="sxs-lookup"><span data-stu-id="510af-105">ClientCertByTpByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -Thumbprint <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="510af-106">ClientCertByCnTpName</span><span class="sxs-lookup"><span data-stu-id="510af-106">ClientCertByCnTpName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="510af-107">ClientCertByCnByName</span><span class="sxs-lookup"><span data-stu-id="510af-107">ClientCertByCnByName</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="510af-108">ClientCertByCnByObj</span><span class="sxs-lookup"><span data-stu-id="510af-108">ClientCertByCnByObj</span></span>
```
Remove-AzServiceFabricManagedClusterClientCertificate [-InputObject] <PSManagedCluster> -CommonName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="510af-109">描述</span><span class="sxs-lookup"><span data-stu-id="510af-109">DESCRIPTION</span></span>
<span data-ttu-id="510af-110">以指紋或通用名稱重新叫用用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="510af-110">Remvoe client certificate by thumbprint or common name.</span></span>

## <span data-ttu-id="510af-111">例子</span><span class="sxs-lookup"><span data-stu-id="510af-111">EXAMPLES</span></span>

### <span data-ttu-id="510af-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="510af-112">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -CommonName 'Contoso.com'
```

<span data-ttu-id="510af-113">使用共同名稱移除用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="510af-113">Remove client certificate by common name.</span></span>

### <span data-ttu-id="510af-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="510af-114">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedClusterClientCertificate -ResourceGroupName $rgName -Name $clusterName -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="510af-115">使用指紋移除用戶端憑證。</span><span class="sxs-lookup"><span data-stu-id="510af-115">Remove client certificate by thumbprint.</span></span>

### <span data-ttu-id="510af-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="510af-116">Example 3</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedClusterClientCertificate -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="510af-117">使用手指列印來移除用戶端憑證，並套用管線。</span><span class="sxs-lookup"><span data-stu-id="510af-117">Remove client certificate by thumbprint, with piping.</span></span>

## <span data-ttu-id="510af-118">參數</span><span class="sxs-lookup"><span data-stu-id="510af-118">PARAMETERS</span></span>

### <span data-ttu-id="510af-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="510af-119">-AsJob</span></span>
<span data-ttu-id="510af-120">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="510af-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="510af-121">-CommonName</span><span class="sxs-lookup"><span data-stu-id="510af-121">-CommonName</span></span>
<span data-ttu-id="510af-122">用戶端憑證通用名稱。</span><span class="sxs-lookup"><span data-stu-id="510af-122">Client certificate common name.</span></span>

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

### <span data-ttu-id="510af-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="510af-123">-DefaultProfile</span></span>
<span data-ttu-id="510af-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="510af-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="510af-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="510af-125">-InputObject</span></span>
<span data-ttu-id="510af-126">受管理的組群資源</span><span class="sxs-lookup"><span data-stu-id="510af-126">Managed cluster resource</span></span>

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

### <span data-ttu-id="510af-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="510af-127">-Name</span></span>
<span data-ttu-id="510af-128">指定組名。</span><span class="sxs-lookup"><span data-stu-id="510af-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="510af-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="510af-129">-PassThru</span></span>
<span data-ttu-id="510af-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="510af-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="510af-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="510af-131">-ResourceGroupName</span></span>
<span data-ttu-id="510af-132">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="510af-132">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="510af-133">-拇指列印</span><span class="sxs-lookup"><span data-stu-id="510af-133">-Thumbprint</span></span>
<span data-ttu-id="510af-134">用戶端憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="510af-134">Client certificate thumbprint.</span></span>

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

### <span data-ttu-id="510af-135">-確認</span><span class="sxs-lookup"><span data-stu-id="510af-135">-Confirm</span></span>
<span data-ttu-id="510af-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="510af-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="510af-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="510af-137">-WhatIf</span></span>
<span data-ttu-id="510af-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="510af-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="510af-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="510af-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="510af-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="510af-140">CommonParameters</span></span>
<span data-ttu-id="510af-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="510af-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="510af-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="510af-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="510af-143">輸入</span><span class="sxs-lookup"><span data-stu-id="510af-143">INPUTS</span></span>

### <span data-ttu-id="510af-144">System.String</span><span class="sxs-lookup"><span data-stu-id="510af-144">System.String</span></span>

## <span data-ttu-id="510af-145">輸出</span><span class="sxs-lookup"><span data-stu-id="510af-145">OUTPUTS</span></span>

### <span data-ttu-id="510af-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="510af-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="510af-147">筆記</span><span class="sxs-lookup"><span data-stu-id="510af-147">NOTES</span></span>

## <span data-ttu-id="510af-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="510af-148">RELATED LINKS</span></span>
