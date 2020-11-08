---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 5c0af3ed67bd7cba3408b6628de70c7064120954
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137960"
---
# <span data-ttu-id="07125-101">New-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="07125-101">New-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="07125-102">摘要</span><span class="sxs-lookup"><span data-stu-id="07125-102">SYNOPSIS</span></span>
<span data-ttu-id="07125-103">在裝置上的 Edge 儲存空間帳戶中建立新的儲存空間容器。</span><span class="sxs-lookup"><span data-stu-id="07125-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="07125-104">句法</span><span class="sxs-lookup"><span data-stu-id="07125-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07125-105">說明</span><span class="sxs-lookup"><span data-stu-id="07125-105">DESCRIPTION</span></span>
<span data-ttu-id="07125-106">**新的-AzStackEdgeStorageContainer** Cmdlet 會在堆疊 edge 裝置的 Edge 儲存空間帳戶中建立新的儲存空間容器。</span><span class="sxs-lookup"><span data-stu-id="07125-106">The **New-AzStackEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Stack Edge device.</span></span>

## <span data-ttu-id="07125-107">示例</span><span class="sxs-lookup"><span data-stu-id="07125-107">EXAMPLES</span></span>

### <span data-ttu-id="07125-108">範例1</span><span class="sxs-lookup"><span data-stu-id="07125-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="07125-109">參數</span><span class="sxs-lookup"><span data-stu-id="07125-109">PARAMETERS</span></span>

### <span data-ttu-id="07125-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07125-110">-AsJob</span></span>
<span data-ttu-id="07125-111">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="07125-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07125-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="07125-112">-DataFormat</span></span>
<span data-ttu-id="07125-113">設定資料格式 ex： PageBlob、BlobBlob</span><span class="sxs-lookup"><span data-stu-id="07125-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="07125-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07125-114">-DefaultProfile</span></span>
<span data-ttu-id="07125-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="07125-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07125-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="07125-116">-DeviceName</span></span>
<span data-ttu-id="07125-117">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="07125-117">Device Name</span></span>

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

### <span data-ttu-id="07125-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="07125-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="07125-119">提供現有 EdgeStorageAccount 的名稱</span><span class="sxs-lookup"><span data-stu-id="07125-119">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="07125-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="07125-120">-Name</span></span>
<span data-ttu-id="07125-121">資源名稱</span><span class="sxs-lookup"><span data-stu-id="07125-121">Resource Name</span></span>

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

### <span data-ttu-id="07125-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07125-122">-ResourceGroupName</span></span>
<span data-ttu-id="07125-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="07125-123">Resource Group Name</span></span>

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

### <span data-ttu-id="07125-124">-確認</span><span class="sxs-lookup"><span data-stu-id="07125-124">-Confirm</span></span>
<span data-ttu-id="07125-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="07125-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07125-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07125-126">-WhatIf</span></span>
<span data-ttu-id="07125-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="07125-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07125-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07125-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07125-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07125-129">CommonParameters</span></span>
<span data-ttu-id="07125-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="07125-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07125-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="07125-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07125-132">輸入</span><span class="sxs-lookup"><span data-stu-id="07125-132">INPUTS</span></span>

### <span data-ttu-id="07125-133">System.object</span><span class="sxs-lookup"><span data-stu-id="07125-133">System.String</span></span>

## <span data-ttu-id="07125-134">輸出</span><span class="sxs-lookup"><span data-stu-id="07125-134">OUTPUTS</span></span>

### <span data-ttu-id="07125-135">PSStackEdgeStorageContainer （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="07125-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="07125-136">筆記</span><span class="sxs-lookup"><span data-stu-id="07125-136">NOTES</span></span>

## <span data-ttu-id="07125-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="07125-137">RELATED LINKS</span></span>