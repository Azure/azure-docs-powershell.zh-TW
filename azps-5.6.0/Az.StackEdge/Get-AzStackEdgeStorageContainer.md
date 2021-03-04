---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 71540063e9eb4323d94a579df8f6489719f7c3fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916856"
---
# <span data-ttu-id="1f74c-101">Get-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1f74c-101">Get-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="1f74c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1f74c-102">SYNOPSIS</span></span>
<span data-ttu-id="1f74c-103">在裝置上獲取 Edge 儲存空間帳戶的容器。</span><span class="sxs-lookup"><span data-stu-id="1f74c-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="1f74c-104">語法</span><span class="sxs-lookup"><span data-stu-id="1f74c-104">SYNTAX</span></span>

### <span data-ttu-id="1f74c-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1f74c-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f74c-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f74c-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f74c-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f74c-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f74c-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f74c-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSStackEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="1f74c-109">描述</span><span class="sxs-lookup"><span data-stu-id="1f74c-109">DESCRIPTION</span></span>
<span data-ttu-id="1f74c-110">**Get-AzStackEdgeStorageContainer Cmdlet** 會取得 Stack Edge 裝置上 Edge 儲存空間帳戶的儲存容器。</span><span class="sxs-lookup"><span data-stu-id="1f74c-110">The **Get-AzStackEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="1f74c-111">您可以在 Cmdlet 中將名稱指定為參數，以抓取特定儲存容器的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="1f74c-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="1f74c-112">例子</span><span class="sxs-lookup"><span data-stu-id="1f74c-112">EXAMPLES</span></span>

### <span data-ttu-id="1f74c-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="1f74c-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="1f74c-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="1f74c-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="1f74c-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="1f74c-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzStackEdgeStorageAccount | Get-AzStackEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="1f74c-116">參數</span><span class="sxs-lookup"><span data-stu-id="1f74c-116">PARAMETERS</span></span>

### <span data-ttu-id="1f74c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f74c-117">-DefaultProfile</span></span>
<span data-ttu-id="1f74c-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f74c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f74c-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1f74c-119">-DeviceName</span></span>
<span data-ttu-id="1f74c-120">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="1f74c-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f74c-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1f74c-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="1f74c-122">提供現有的 EdgeStorageAccount名稱</span><span class="sxs-lookup"><span data-stu-id="1f74c-122">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f74c-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="1f74c-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="1f74c-124">提供現有的 EdgeStorageAccount 物件</span><span class="sxs-lookup"><span data-stu-id="1f74c-124">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f74c-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f74c-125">-Name</span></span>
<span data-ttu-id="1f74c-126">EdgeStorageContainer 的名稱</span><span class="sxs-lookup"><span data-stu-id="1f74c-126">Name of the EdgeStorageContainer</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageContainerName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f74c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f74c-127">-ResourceGroupName</span></span>
<span data-ttu-id="1f74c-128">資源組名</span><span class="sxs-lookup"><span data-stu-id="1f74c-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f74c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f74c-129">-ResourceId</span></span>
<span data-ttu-id="1f74c-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f74c-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f74c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f74c-131">CommonParameters</span></span>
<span data-ttu-id="1f74c-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1f74c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f74c-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f74c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f74c-134">輸入</span><span class="sxs-lookup"><span data-stu-id="1f74c-134">INPUTS</span></span>

### <span data-ttu-id="1f74c-135">System.String</span><span class="sxs-lookup"><span data-stu-id="1f74c-135">System.String</span></span>

### <span data-ttu-id="1f74c-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1f74c-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="1f74c-137">輸出</span><span class="sxs-lookup"><span data-stu-id="1f74c-137">OUTPUTS</span></span>

### <span data-ttu-id="1f74c-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1f74c-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="1f74c-139">筆記</span><span class="sxs-lookup"><span data-stu-id="1f74c-139">NOTES</span></span>

## <span data-ttu-id="1f74c-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f74c-140">RELATED LINKS</span></span>
