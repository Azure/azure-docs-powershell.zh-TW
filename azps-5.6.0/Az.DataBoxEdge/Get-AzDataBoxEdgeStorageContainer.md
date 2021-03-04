---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: fb60583922fd01d2f3a472525f3210b070fb5935
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914873"
---
# <span data-ttu-id="d4ec1-101">Get-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d4ec1-101">Get-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="d4ec1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d4ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="d4ec1-103">在裝置上獲取 Edge 儲存空間帳戶的容器。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="d4ec1-104">語法</span><span class="sxs-lookup"><span data-stu-id="d4ec1-104">SYNTAX</span></span>

### <span data-ttu-id="d4ec1-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d4ec1-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4ec1-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4ec1-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4ec1-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4ec1-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d4ec1-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4ec1-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSDataBoxEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="d4ec1-109">描述</span><span class="sxs-lookup"><span data-stu-id="d4ec1-109">DESCRIPTION</span></span>
<span data-ttu-id="d4ec1-110">**Get-AzDataBoxEdgeStorageContainer Cmdlet** 會取得 Data Box Edge 裝置上 Edge 儲存空間帳戶的儲存容器。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-110">The **Get-AzDataBoxEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="d4ec1-111">您可以在 Cmdlet 中將名稱指定為參數，以抓取特定儲存容器的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="d4ec1-112">例子</span><span class="sxs-lookup"><span data-stu-id="d4ec1-112">EXAMPLES</span></span>

### <span data-ttu-id="d4ec1-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="d4ec1-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="d4ec1-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="d4ec1-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="d4ec1-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="d4ec1-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount | Get-AzDataBoxEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="d4ec1-116">參數</span><span class="sxs-lookup"><span data-stu-id="d4ec1-116">PARAMETERS</span></span>

### <span data-ttu-id="d4ec1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4ec1-117">-DefaultProfile</span></span>
<span data-ttu-id="d4ec1-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4ec1-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d4ec1-119">-DeviceName</span></span>
<span data-ttu-id="d4ec1-120">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="d4ec1-120">Device Name</span></span>

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

### <span data-ttu-id="d4ec1-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d4ec1-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="d4ec1-122">提供現有的 EdgeStorageAccount名稱</span><span class="sxs-lookup"><span data-stu-id="d4ec1-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="d4ec1-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="d4ec1-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="d4ec1-124">提供現有的 EdgeStorageAccount 物件</span><span class="sxs-lookup"><span data-stu-id="d4ec1-124">Provide existing EdgeStorageAccount Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4ec1-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="d4ec1-125">-Name</span></span>
<span data-ttu-id="d4ec1-126">EdgeStorageContainer 的名稱</span><span class="sxs-lookup"><span data-stu-id="d4ec1-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="d4ec1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4ec1-127">-ResourceGroupName</span></span>
<span data-ttu-id="d4ec1-128">資源組名</span><span class="sxs-lookup"><span data-stu-id="d4ec1-128">Resource Group Name</span></span>

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

### <span data-ttu-id="d4ec1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4ec1-129">-ResourceId</span></span>
<span data-ttu-id="d4ec1-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4ec1-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="d4ec1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4ec1-131">CommonParameters</span></span>
<span data-ttu-id="d4ec1-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d4ec1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4ec1-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4ec1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4ec1-134">輸入</span><span class="sxs-lookup"><span data-stu-id="d4ec1-134">INPUTS</span></span>

### <span data-ttu-id="d4ec1-135">System.String</span><span class="sxs-lookup"><span data-stu-id="d4ec1-135">System.String</span></span>

### <span data-ttu-id="d4ec1-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d4ec1-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="d4ec1-137">輸出</span><span class="sxs-lookup"><span data-stu-id="d4ec1-137">OUTPUTS</span></span>

### <span data-ttu-id="d4ec1-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d4ec1-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="d4ec1-139">筆記</span><span class="sxs-lookup"><span data-stu-id="d4ec1-139">NOTES</span></span>

## <span data-ttu-id="d4ec1-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4ec1-140">RELATED LINKS</span></span>
