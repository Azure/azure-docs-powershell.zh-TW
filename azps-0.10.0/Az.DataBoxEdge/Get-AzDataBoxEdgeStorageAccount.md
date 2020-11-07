---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: aa9b6f8c3edfc25fc74f8351fa14bfa74577cf0c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795781"
---
# <span data-ttu-id="f6e45-101">Get-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f6e45-101">Get-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="f6e45-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6e45-102">SYNOPSIS</span></span>
<span data-ttu-id="f6e45-103">取得裝置上的邊緣儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="f6e45-103">Gets the Edge Storage accounts on the device.</span></span>

## <span data-ttu-id="f6e45-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6e45-104">SYNTAX</span></span>

### <span data-ttu-id="f6e45-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f6e45-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6e45-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6e45-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f6e45-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6e45-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6e45-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6e45-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccount [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="f6e45-109">說明</span><span class="sxs-lookup"><span data-stu-id="f6e45-109">DESCRIPTION</span></span>
<span data-ttu-id="f6e45-110">**AzDataBoxEdgeStorageAccount** Cmdlet 會取得資料盒 edge 裝置上可用的 Edge 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="f6e45-110">The **Get-AzDataBoxEdgeStorageAccount** cmdlet gets the Edge Storage accounts available on a Data Box Edge device.</span></span> <span data-ttu-id="f6e45-111">您可以將名稱指定為 Cmdlet 中的參數，以取得特定 Edge 儲存空間帳戶的資訊。</span><span class="sxs-lookup"><span data-stu-id="f6e45-111">You can specify the Name as a parameter in the cmdlet to get the information of a specific Edge Storage account.</span></span>

## <span data-ttu-id="f6e45-112">示例</span><span class="sxs-lookup"><span data-stu-id="f6e45-112">EXAMPLES</span></span>

### <span data-ttu-id="f6e45-113">範例2</span><span class="sxs-lookup"><span data-stu-id="f6e45-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge -Name edgestoragegacount1

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName
```

### <span data-ttu-id="f6e45-114">範例2</span><span class="sxs-lookup"><span data-stu-id="f6e45-114">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -ResourceGroupName rgpName -DeviceName db-edge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="f6e45-115">範例3</span><span class="sxs-lookup"><span data-stu-id="f6e45-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeDevice -ResourceGroupName rgpName -DeviceName db-edge | Get-AzDataBoxEdgeStorageAccount

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

### <span data-ttu-id="f6e45-116">範例4</span><span class="sxs-lookup"><span data-stu-id="f6e45-116">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeStorageAccount -DeviceObject $dbEdge

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 2              OK     https://edgestoragegacount1.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount1    db-edge    rgpName          
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.db-edge.microsoftdatabox.com/ cloudstorageaccount2    db-edge    rgpName
```

## <span data-ttu-id="f6e45-117">參數</span><span class="sxs-lookup"><span data-stu-id="f6e45-117">PARAMETERS</span></span>

### <span data-ttu-id="f6e45-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6e45-118">-DefaultProfile</span></span>
<span data-ttu-id="f6e45-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6e45-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6e45-120">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f6e45-120">-DeviceName</span></span>
<span data-ttu-id="f6e45-121">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="f6e45-121">Device Name</span></span>

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

### <span data-ttu-id="f6e45-122">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="f6e45-122">-DeviceObject</span></span>
<span data-ttu-id="f6e45-123">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="f6e45-123">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6e45-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6e45-124">-Name</span></span>
<span data-ttu-id="f6e45-125">資源名稱</span><span class="sxs-lookup"><span data-stu-id="f6e45-125">Resource Name</span></span>

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

### <span data-ttu-id="f6e45-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6e45-126">-ResourceGroupName</span></span>
<span data-ttu-id="f6e45-127">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f6e45-127">Resource Group Name</span></span>

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

### <span data-ttu-id="f6e45-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6e45-128">-ResourceId</span></span>
<span data-ttu-id="f6e45-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6e45-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="f6e45-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6e45-130">CommonParameters</span></span>
<span data-ttu-id="f6e45-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6e45-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6e45-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f6e45-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6e45-133">輸入</span><span class="sxs-lookup"><span data-stu-id="f6e45-133">INPUTS</span></span>

### <span data-ttu-id="f6e45-134">System.object</span><span class="sxs-lookup"><span data-stu-id="f6e45-134">System.String</span></span>

### <span data-ttu-id="f6e45-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f6e45-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="f6e45-136">輸出</span><span class="sxs-lookup"><span data-stu-id="f6e45-136">OUTPUTS</span></span>

### <span data-ttu-id="f6e45-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f6e45-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="f6e45-138">筆記</span><span class="sxs-lookup"><span data-stu-id="f6e45-138">NOTES</span></span>

## <span data-ttu-id="f6e45-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6e45-139">RELATED LINKS</span></span>
