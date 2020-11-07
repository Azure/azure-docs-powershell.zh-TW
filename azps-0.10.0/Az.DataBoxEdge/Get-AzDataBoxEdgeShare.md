---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeShare.md
ms.openlocfilehash: 9bcc19d29bf372aaa0b1c59e23f53e80edde4d17
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795782"
---
# <span data-ttu-id="71ce4-101">Get-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="71ce4-101">Get-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="71ce4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="71ce4-103">取得裝置的可用共用。</span><span class="sxs-lookup"><span data-stu-id="71ce4-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="71ce4-104">句法</span><span class="sxs-lookup"><span data-stu-id="71ce4-104">SYNTAX</span></span>

### <span data-ttu-id="71ce4-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="71ce4-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71ce4-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71ce4-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71ce4-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="71ce4-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71ce4-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71ce4-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="71ce4-109">說明</span><span class="sxs-lookup"><span data-stu-id="71ce4-109">DESCRIPTION</span></span>
<span data-ttu-id="71ce4-110">**AzDataBoxEdgeShare** Cmdlet 會取得資料編輯方塊邊緣裝置的可用共用。</span><span class="sxs-lookup"><span data-stu-id="71ce4-110">The **Get-AzDataBoxEdgeShare** cmdlet gets the available shares for a Data Box Edge device.</span></span> <span data-ttu-id="71ce4-111">如果提供 Name，就會透過名稱取得共用。</span><span class="sxs-lookup"><span data-stu-id="71ce4-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="71ce4-112">示例</span><span class="sxs-lookup"><span data-stu-id="71ce4-112">EXAMPLES</span></span>

### <span data-ttu-id="71ce4-113">範例1</span><span class="sxs-lookup"><span data-stu-id="71ce4-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="71ce4-114">參數</span><span class="sxs-lookup"><span data-stu-id="71ce4-114">PARAMETERS</span></span>

### <span data-ttu-id="71ce4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71ce4-115">-DefaultProfile</span></span>
<span data-ttu-id="71ce4-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="71ce4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71ce4-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="71ce4-117">-DeviceName</span></span>
<span data-ttu-id="71ce4-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="71ce4-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71ce4-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="71ce4-119">-DeviceObject</span></span>
<span data-ttu-id="71ce4-120">請提供相對應的裝置物件</span><span class="sxs-lookup"><span data-stu-id="71ce4-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="71ce4-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="71ce4-121">-Name</span></span>
<span data-ttu-id="71ce4-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="71ce4-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71ce4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71ce4-123">-ResourceGroupName</span></span>
<span data-ttu-id="71ce4-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="71ce4-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71ce4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71ce4-125">-ResourceId</span></span>
<span data-ttu-id="71ce4-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="71ce4-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71ce4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71ce4-127">CommonParameters</span></span>
<span data-ttu-id="71ce4-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71ce4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71ce4-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="71ce4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71ce4-130">輸入</span><span class="sxs-lookup"><span data-stu-id="71ce4-130">INPUTS</span></span>

### <span data-ttu-id="71ce4-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="71ce4-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="71ce4-132">輸出</span><span class="sxs-lookup"><span data-stu-id="71ce4-132">OUTPUTS</span></span>

### <span data-ttu-id="71ce4-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="71ce4-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="71ce4-134">筆記</span><span class="sxs-lookup"><span data-stu-id="71ce4-134">NOTES</span></span>

## <span data-ttu-id="71ce4-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="71ce4-135">RELATED LINKS</span></span>
