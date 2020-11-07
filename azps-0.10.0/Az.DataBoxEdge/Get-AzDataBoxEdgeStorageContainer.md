---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 174f6c58dfeb2d79a19b08cc1f360ea05e0c4736
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795773"
---
# <span data-ttu-id="14bd2-101">Get-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="14bd2-101">Get-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="14bd2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="14bd2-103">取得裝置上 Edge 儲存空間帳戶的容器。</span><span class="sxs-lookup"><span data-stu-id="14bd2-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="14bd2-104">句法</span><span class="sxs-lookup"><span data-stu-id="14bd2-104">SYNTAX</span></span>

### <span data-ttu-id="14bd2-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="14bd2-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14bd2-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14bd2-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="14bd2-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="14bd2-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="14bd2-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14bd2-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSDataBoxEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="14bd2-109">說明</span><span class="sxs-lookup"><span data-stu-id="14bd2-109">DESCRIPTION</span></span>
<span data-ttu-id="14bd2-110">**AzDataBoxEdgeStorageContainer** Cmdlet 會取得資料盒 edge 裝置上 Edge 儲存空間帳戶的儲存容器。</span><span class="sxs-lookup"><span data-stu-id="14bd2-110">The **Get-AzDataBoxEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="14bd2-111">您可以將名稱指定為 Cmdlet 中的參數，以取得特定儲存空間容器的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="14bd2-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="14bd2-112">示例</span><span class="sxs-lookup"><span data-stu-id="14bd2-112">EXAMPLES</span></span>

### <span data-ttu-id="14bd2-113">範例1</span><span class="sxs-lookup"><span data-stu-id="14bd2-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="14bd2-114">範例2</span><span class="sxs-lookup"><span data-stu-id="14bd2-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="14bd2-115">範例3</span><span class="sxs-lookup"><span data-stu-id="14bd2-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount | Get-AzDataBoxEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="14bd2-116">參數</span><span class="sxs-lookup"><span data-stu-id="14bd2-116">PARAMETERS</span></span>

### <span data-ttu-id="14bd2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14bd2-117">-DefaultProfile</span></span>
<span data-ttu-id="14bd2-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="14bd2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14bd2-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="14bd2-119">-DeviceName</span></span>
<span data-ttu-id="14bd2-120">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="14bd2-120">Device Name</span></span>

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

### <span data-ttu-id="14bd2-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="14bd2-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="14bd2-122">提供現有 EdgeStorageAccount 的名稱</span><span class="sxs-lookup"><span data-stu-id="14bd2-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="14bd2-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="14bd2-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="14bd2-124">提供現有的 EdgeStorageAccount 物件</span><span class="sxs-lookup"><span data-stu-id="14bd2-124">Provide existing EdgeStorageAccount Object</span></span>

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

### <span data-ttu-id="14bd2-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="14bd2-125">-Name</span></span>
<span data-ttu-id="14bd2-126">EdgeStorageContainer 的名稱</span><span class="sxs-lookup"><span data-stu-id="14bd2-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="14bd2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14bd2-127">-ResourceGroupName</span></span>
<span data-ttu-id="14bd2-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="14bd2-128">Resource Group Name</span></span>

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

### <span data-ttu-id="14bd2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14bd2-129">-ResourceId</span></span>
<span data-ttu-id="14bd2-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="14bd2-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="14bd2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14bd2-131">CommonParameters</span></span>
<span data-ttu-id="14bd2-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14bd2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14bd2-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="14bd2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14bd2-134">輸入</span><span class="sxs-lookup"><span data-stu-id="14bd2-134">INPUTS</span></span>

### <span data-ttu-id="14bd2-135">System.object</span><span class="sxs-lookup"><span data-stu-id="14bd2-135">System.String</span></span>

### <span data-ttu-id="14bd2-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="14bd2-136">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="14bd2-137">輸出</span><span class="sxs-lookup"><span data-stu-id="14bd2-137">OUTPUTS</span></span>

### <span data-ttu-id="14bd2-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="14bd2-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="14bd2-139">筆記</span><span class="sxs-lookup"><span data-stu-id="14bd2-139">NOTES</span></span>

## <span data-ttu-id="14bd2-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="14bd2-140">RELATED LINKS</span></span>
