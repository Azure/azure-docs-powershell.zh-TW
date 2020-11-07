---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: e4283b23fb4a82c17f35354d854c30c3ec1b2329
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796173"
---
# <span data-ttu-id="e43f2-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="e43f2-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="e43f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e43f2-102">SYNOPSIS</span></span>
<span data-ttu-id="e43f2-103">授與快照存取權。</span><span class="sxs-lookup"><span data-stu-id="e43f2-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="e43f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="e43f2-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e43f2-105">說明</span><span class="sxs-lookup"><span data-stu-id="e43f2-105">DESCRIPTION</span></span>
<span data-ttu-id="e43f2-106">**Grant AzSnapshotAccess** Cmdlet 會授權存取快照。</span><span class="sxs-lookup"><span data-stu-id="e43f2-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="e43f2-107">示例</span><span class="sxs-lookup"><span data-stu-id="e43f2-107">EXAMPLES</span></span>

### <span data-ttu-id="e43f2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e43f2-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="e43f2-109">針對60秒的資源群組中名為「Snapshot01」的快照，授與「Read」的存取權。</span><span class="sxs-lookup"><span data-stu-id="e43f2-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="e43f2-110">參數</span><span class="sxs-lookup"><span data-stu-id="e43f2-110">PARAMETERS</span></span>

### <span data-ttu-id="e43f2-111">-Access</span><span class="sxs-lookup"><span data-stu-id="e43f2-111">-Access</span></span>
<span data-ttu-id="e43f2-112">指定存取層級。</span><span class="sxs-lookup"><span data-stu-id="e43f2-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e43f2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e43f2-113">-AsJob</span></span>
<span data-ttu-id="e43f2-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e43f2-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e43f2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e43f2-115">-DefaultProfile</span></span>
<span data-ttu-id="e43f2-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e43f2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e43f2-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="e43f2-117">-DurationInSecond</span></span>
<span data-ttu-id="e43f2-118">指定存取持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e43f2-118">Specifies access duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e43f2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e43f2-119">-ResourceGroupName</span></span>
<span data-ttu-id="e43f2-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e43f2-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e43f2-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="e43f2-121">-SnapshotName</span></span>
<span data-ttu-id="e43f2-122">指定快照的名稱。</span><span class="sxs-lookup"><span data-stu-id="e43f2-122">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e43f2-123">-確認</span><span class="sxs-lookup"><span data-stu-id="e43f2-123">-Confirm</span></span>
<span data-ttu-id="e43f2-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e43f2-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e43f2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e43f2-125">-WhatIf</span></span>
<span data-ttu-id="e43f2-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e43f2-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e43f2-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e43f2-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e43f2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e43f2-128">CommonParameters</span></span>
<span data-ttu-id="e43f2-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e43f2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e43f2-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e43f2-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e43f2-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e43f2-131">INPUTS</span></span>

### <span data-ttu-id="e43f2-132">System.object</span><span class="sxs-lookup"><span data-stu-id="e43f2-132">System.String</span></span>

## <span data-ttu-id="e43f2-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e43f2-133">OUTPUTS</span></span>

### <span data-ttu-id="e43f2-134">System.object</span><span class="sxs-lookup"><span data-stu-id="e43f2-134">System.Object</span></span>

## <span data-ttu-id="e43f2-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e43f2-135">NOTES</span></span>

## <span data-ttu-id="e43f2-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e43f2-136">RELATED LINKS</span></span>

