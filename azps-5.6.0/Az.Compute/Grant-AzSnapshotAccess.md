---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: 215ae1149cdfd939db242907a00b82b1e9fd82a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914893"
---
# <span data-ttu-id="9dc81-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="9dc81-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="9dc81-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9dc81-102">SYNOPSIS</span></span>
<span data-ttu-id="9dc81-103">授予快照的存取權。</span><span class="sxs-lookup"><span data-stu-id="9dc81-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="9dc81-104">語法</span><span class="sxs-lookup"><span data-stu-id="9dc81-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9dc81-105">描述</span><span class="sxs-lookup"><span data-stu-id="9dc81-105">DESCRIPTION</span></span>
<span data-ttu-id="9dc81-106">**Grant-AzSnapshotAccess** Cmdlet 會授予快照的存取權。</span><span class="sxs-lookup"><span data-stu-id="9dc81-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="9dc81-107">例子</span><span class="sxs-lookup"><span data-stu-id="9dc81-107">EXAMPLES</span></span>

### <span data-ttu-id="9dc81-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="9dc81-108">Example 1</span></span>
```
PS C:\> Grant-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="9dc81-109">在名為 "ResourceGroup01" 的資源群組中，將名為 "Snapshot01" 的快照授予 60 秒的讀取存取權。</span><span class="sxs-lookup"><span data-stu-id="9dc81-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="9dc81-110">參數</span><span class="sxs-lookup"><span data-stu-id="9dc81-110">PARAMETERS</span></span>

### <span data-ttu-id="9dc81-111">-Access</span><span class="sxs-lookup"><span data-stu-id="9dc81-111">-Access</span></span>
<span data-ttu-id="9dc81-112">指定 Access 層級。</span><span class="sxs-lookup"><span data-stu-id="9dc81-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc81-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9dc81-113">-AsJob</span></span>
<span data-ttu-id="9dc81-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9dc81-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9dc81-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dc81-115">-DefaultProfile</span></span>
<span data-ttu-id="9dc81-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9dc81-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9dc81-117">-DurationIn用</span><span class="sxs-lookup"><span data-stu-id="9dc81-117">-DurationInSecond</span></span>
<span data-ttu-id="9dc81-118">以秒數指定存取持續時間。</span><span class="sxs-lookup"><span data-stu-id="9dc81-118">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dc81-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dc81-119">-ResourceGroupName</span></span>
<span data-ttu-id="9dc81-120">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9dc81-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9dc81-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="9dc81-121">-SnapshotName</span></span>
<span data-ttu-id="9dc81-122">指定快照名稱。</span><span class="sxs-lookup"><span data-stu-id="9dc81-122">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9dc81-123">-確認</span><span class="sxs-lookup"><span data-stu-id="9dc81-123">-Confirm</span></span>
<span data-ttu-id="9dc81-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9dc81-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dc81-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dc81-125">-WhatIf</span></span>
<span data-ttu-id="9dc81-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9dc81-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9dc81-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9dc81-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dc81-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dc81-128">CommonParameters</span></span>
<span data-ttu-id="9dc81-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9dc81-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dc81-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9dc81-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dc81-131">輸入</span><span class="sxs-lookup"><span data-stu-id="9dc81-131">INPUTS</span></span>

### <span data-ttu-id="9dc81-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9dc81-132">System.String</span></span>

## <span data-ttu-id="9dc81-133">輸出</span><span class="sxs-lookup"><span data-stu-id="9dc81-133">OUTPUTS</span></span>

### <span data-ttu-id="9dc81-134">Microsoft.Azure.Commands.Compute.Automation.models.PSAccesssUri</span><span class="sxs-lookup"><span data-stu-id="9dc81-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="9dc81-135">筆記</span><span class="sxs-lookup"><span data-stu-id="9dc81-135">NOTES</span></span>

## <span data-ttu-id="9dc81-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="9dc81-136">RELATED LINKS</span></span>
