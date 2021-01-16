---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 0b18183b27f5701036afb74bb85768b48e9492e8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276747"
---
# <span data-ttu-id="e3115-101">Get-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e3115-101">Get-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="e3115-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3115-102">SYNOPSIS</span></span>
<span data-ttu-id="e3115-103">取得裝置上 Edge 儲存空間帳戶的容器。</span><span class="sxs-lookup"><span data-stu-id="e3115-103">Gets the containers for an Edge Storage account on a device.</span></span>

## <span data-ttu-id="e3115-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3115-104">SYNTAX</span></span>

### <span data-ttu-id="e3115-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e3115-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3115-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3115-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3115-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3115-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3115-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3115-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageContainer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -EdgeStorageAccountObject <PSStackEdgeStorageAccount> [<CommonParameters>]
```

## <span data-ttu-id="e3115-109">說明</span><span class="sxs-lookup"><span data-stu-id="e3115-109">DESCRIPTION</span></span>
<span data-ttu-id="e3115-110">**AzStackEdgeStorageContainer** Cmdlet 會取得堆疊 edge 裝置上 Edge 儲存空間帳戶的儲存容器。</span><span class="sxs-lookup"><span data-stu-id="e3115-110">The **Get-AzStackEdgeStorageContainer** cmdlet gets the storage container for an Edge Storage account on a Stack Edge device.</span></span> <span data-ttu-id="e3115-111">您可以將名稱指定為 Cmdlet 中的參數，以取得特定儲存空間容器的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e3115-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific storage container.</span></span> 

## <span data-ttu-id="e3115-112">示例</span><span class="sxs-lookup"><span data-stu-id="e3115-112">EXAMPLES</span></span>

### <span data-ttu-id="e3115-113">範例1</span><span class="sxs-lookup"><span data-stu-id="e3115-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name container1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="e3115-114">範例2</span><span class="sxs-lookup"><span data-stu-id="e3115-114">Example 2</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
```

### <span data-ttu-id="e3115-115">範例3</span><span class="sxs-lookup"><span data-stu-id="e3115-115">Example 3</span></span>
```powershell
PS C:\>  Get-AzStackEdgeDevice -ResourceGroupName resourceGroupName -DeviceName db-edge | Get-AzStackEdgeStorageAccount | Get-AzStackEdgeStorageContainer
Name       DataFormat Status EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ------ ---------------------- ---------- -----------------
container1 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container2 BlockBlob  Ok     edgestorageaccount1    db-edge    resourceGroupName
container4 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
container5 BlockBlob  Ok     edgestorageaccount2    db-edge    resourceGroupName
```

## <span data-ttu-id="e3115-116">參數</span><span class="sxs-lookup"><span data-stu-id="e3115-116">PARAMETERS</span></span>

### <span data-ttu-id="e3115-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3115-117">-DefaultProfile</span></span>
<span data-ttu-id="e3115-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3115-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3115-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e3115-119">-DeviceName</span></span>
<span data-ttu-id="e3115-120">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="e3115-120">Device Name</span></span>

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

### <span data-ttu-id="e3115-121">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e3115-121">-EdgeStorageAccountName</span></span>
<span data-ttu-id="e3115-122">提供現有 EdgeStorageAccount 的名稱</span><span class="sxs-lookup"><span data-stu-id="e3115-122">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="e3115-123">-EdgeStorageAccountObject</span><span class="sxs-lookup"><span data-stu-id="e3115-123">-EdgeStorageAccountObject</span></span>
<span data-ttu-id="e3115-124">提供現有的 EdgeStorageAccount 物件</span><span class="sxs-lookup"><span data-stu-id="e3115-124">Provide existing EdgeStorageAccount Object</span></span>

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

### <span data-ttu-id="e3115-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3115-125">-Name</span></span>
<span data-ttu-id="e3115-126">EdgeStorageContainer 的名稱</span><span class="sxs-lookup"><span data-stu-id="e3115-126">Name of the EdgeStorageContainer</span></span>

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

### <span data-ttu-id="e3115-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3115-127">-ResourceGroupName</span></span>
<span data-ttu-id="e3115-128">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="e3115-128">Resource Group Name</span></span>

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

### <span data-ttu-id="e3115-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3115-129">-ResourceId</span></span>
<span data-ttu-id="e3115-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3115-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="e3115-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3115-131">CommonParameters</span></span>
<span data-ttu-id="e3115-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3115-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3115-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e3115-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3115-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e3115-134">INPUTS</span></span>

### <span data-ttu-id="e3115-135">System.object</span><span class="sxs-lookup"><span data-stu-id="e3115-135">System.String</span></span>

### <span data-ttu-id="e3115-136">PSStackEdgeStorageAccount （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="e3115-136">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="e3115-137">輸出</span><span class="sxs-lookup"><span data-stu-id="e3115-137">OUTPUTS</span></span>

### <span data-ttu-id="e3115-138">PSStackEdgeStorageContainer （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="e3115-138">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="e3115-139">筆記</span><span class="sxs-lookup"><span data-stu-id="e3115-139">NOTES</span></span>

## <span data-ttu-id="e3115-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3115-140">RELATED LINKS</span></span>
