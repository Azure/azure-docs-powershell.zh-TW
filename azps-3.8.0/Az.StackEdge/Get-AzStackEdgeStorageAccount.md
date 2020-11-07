---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 59d01af85279414503b765aea7f326a8670ec1c2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957000"
---
# <span data-ttu-id="5bebf-101">Get-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5bebf-101">Get-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="5bebf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5bebf-102">SYNOPSIS</span></span>
<span data-ttu-id="5bebf-103">取得裝置上的邊緣儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="5bebf-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="5bebf-104">句法</span><span class="sxs-lookup"><span data-stu-id="5bebf-104">SYNTAX</span></span>

### <span data-ttu-id="5bebf-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5bebf-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bebf-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bebf-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5bebf-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bebf-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bebf-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bebf-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="5bebf-109">說明</span><span class="sxs-lookup"><span data-stu-id="5bebf-109">DESCRIPTION</span></span>
<span data-ttu-id="5bebf-110">**AzStackEdgeStorageAccount** Cmdlet 會取得堆疊 edge 裝置上可用的 Edge 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="5bebf-110">The **Get-AzStackEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Stack Edge device.</span></span> <span data-ttu-id="5bebf-111">您可以將名稱指定為 Cmdlet 中的參數，以取得特定 Edge 儲存空間帳戶的資訊。</span><span class="sxs-lookup"><span data-stu-id="5bebf-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="5bebf-112">示例</span><span class="sxs-lookup"><span data-stu-id="5bebf-112">EXAMPLES</span></span>

### <span data-ttu-id="5bebf-113">範例2</span><span class="sxs-lookup"><span data-stu-id="5bebf-113">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="5bebf-114">範例2</span><span class="sxs-lookup"><span data-stu-id="5bebf-114">Example 2</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="5bebf-115">範例3</span><span class="sxs-lookup"><span data-stu-id="5bebf-115">Example 3</span></span>
```powershell
PS C:\> Get-AzStackEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzStackEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="5bebf-116">範例4</span><span class="sxs-lookup"><span data-stu-id="5bebf-116">Example 4</span></span>
```powershell
PS C:\> Get-AzStackEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="5bebf-117">參數</span><span class="sxs-lookup"><span data-stu-id="5bebf-117">PARAMETERS</span></span>

### <span data-ttu-id="5bebf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bebf-118">-DefaultProfile</span></span>
<span data-ttu-id="5bebf-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5bebf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bebf-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5bebf-120">-DeviceName</span></span>
<span data-ttu-id="5bebf-121">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="5bebf-121">Device Name</span></span>

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

### <span data-ttu-id="5bebf-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="5bebf-122">-DeviceObject</span></span>
<span data-ttu-id="5bebf-123">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="5bebf-123">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bebf-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="5bebf-124">-Name</span></span>
<span data-ttu-id="5bebf-125">資源名稱</span><span class="sxs-lookup"><span data-stu-id="5bebf-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeStorageAccountName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bebf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bebf-126">-ResourceGroupName</span></span>
<span data-ttu-id="5bebf-127">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="5bebf-127">Resource Group Name</span></span>

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

### <span data-ttu-id="5bebf-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bebf-128">-ResourceId</span></span>
<span data-ttu-id="5bebf-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bebf-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bebf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bebf-130">CommonParameters</span></span>
<span data-ttu-id="5bebf-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5bebf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bebf-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5bebf-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bebf-133">輸入</span><span class="sxs-lookup"><span data-stu-id="5bebf-133">INPUTS</span></span>

### <span data-ttu-id="5bebf-134">System.object</span><span class="sxs-lookup"><span data-stu-id="5bebf-134">System.String</span></span>

### <span data-ttu-id="5bebf-135">PSStackEdgeDevice （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="5bebf-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="5bebf-136">輸出</span><span class="sxs-lookup"><span data-stu-id="5bebf-136">OUTPUTS</span></span>

### <span data-ttu-id="5bebf-137">PSStackEdgeStorageAccount （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="5bebf-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="5bebf-138">筆記</span><span class="sxs-lookup"><span data-stu-id="5bebf-138">NOTES</span></span>

## <span data-ttu-id="5bebf-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="5bebf-139">RELATED LINKS</span></span>
