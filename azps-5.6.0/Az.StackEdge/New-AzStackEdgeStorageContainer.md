---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
ms.openlocfilehash: a0fe5dd999d4e5bf8f03d4567e2ba605d42f9cd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915182"
---
# <span data-ttu-id="7fcb8-101">New-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7fcb8-101">New-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="7fcb8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7fcb8-102">SYNOPSIS</span></span>
<span data-ttu-id="7fcb8-103">在裝置上的 Edge 儲存空間帳戶中建立新儲存容器。</span><span class="sxs-lookup"><span data-stu-id="7fcb8-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="7fcb8-104">語法</span><span class="sxs-lookup"><span data-stu-id="7fcb8-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fcb8-105">描述</span><span class="sxs-lookup"><span data-stu-id="7fcb8-105">DESCRIPTION</span></span>
<span data-ttu-id="7fcb8-106">**New-AzStackEdgeStorageContainer Cmdlet** 在 Stack Edge 裝置上的 Edge 儲存空間帳戶中建立新儲存容器。</span><span class="sxs-lookup"><span data-stu-id="7fcb8-106">The **New-AzStackEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Stack Edge device.</span></span>

## <span data-ttu-id="7fcb8-107">例子</span><span class="sxs-lookup"><span data-stu-id="7fcb8-107">EXAMPLES</span></span>

### <span data-ttu-id="7fcb8-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="7fcb8-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="7fcb8-109">參數</span><span class="sxs-lookup"><span data-stu-id="7fcb8-109">PARAMETERS</span></span>

### <span data-ttu-id="7fcb8-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fcb8-110">-AsJob</span></span>
<span data-ttu-id="7fcb8-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7fcb8-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7fcb8-112">-資料格式</span><span class="sxs-lookup"><span data-stu-id="7fcb8-112">-DataFormat</span></span>
<span data-ttu-id="7fcb8-113">設定資料格式，例如：PageBlob、BlobBlob</span><span class="sxs-lookup"><span data-stu-id="7fcb8-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcb8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fcb8-114">-DefaultProfile</span></span>
<span data-ttu-id="7fcb8-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7fcb8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fcb8-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7fcb8-116">-DeviceName</span></span>
<span data-ttu-id="7fcb8-117">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="7fcb8-117">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcb8-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7fcb8-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="7fcb8-119">提供現有的 EdgeStorageAccount名稱</span><span class="sxs-lookup"><span data-stu-id="7fcb8-119">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcb8-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="7fcb8-120">-Name</span></span>
<span data-ttu-id="7fcb8-121">資源名稱</span><span class="sxs-lookup"><span data-stu-id="7fcb8-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcb8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fcb8-122">-ResourceGroupName</span></span>
<span data-ttu-id="7fcb8-123">資源組名</span><span class="sxs-lookup"><span data-stu-id="7fcb8-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcb8-124">-確認</span><span class="sxs-lookup"><span data-stu-id="7fcb8-124">-Confirm</span></span>
<span data-ttu-id="7fcb8-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7fcb8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fcb8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fcb8-126">-WhatIf</span></span>
<span data-ttu-id="7fcb8-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7fcb8-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7fcb8-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7fcb8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fcb8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fcb8-129">CommonParameters</span></span>
<span data-ttu-id="7fcb8-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7fcb8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fcb8-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fcb8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fcb8-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7fcb8-132">INPUTS</span></span>

### <span data-ttu-id="7fcb8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7fcb8-133">System.String</span></span>

## <span data-ttu-id="7fcb8-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7fcb8-134">OUTPUTS</span></span>

### <span data-ttu-id="7fcb8-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7fcb8-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="7fcb8-136">筆記</span><span class="sxs-lookup"><span data-stu-id="7fcb8-136">NOTES</span></span>

## <span data-ttu-id="7fcb8-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="7fcb8-137">RELATED LINKS</span></span>
