---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Grant-AzureRmSnapshotAccess.md
ms.openlocfilehash: b60abc403beea938e24ffaa59e634a36611d150b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449249"
---
# <span data-ttu-id="ec20c-101">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="ec20c-101">Grant-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="ec20c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec20c-102">SYNOPSIS</span></span>
<span data-ttu-id="ec20c-103">授與快照存取權。</span><span class="sxs-lookup"><span data-stu-id="ec20c-103">Grants an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec20c-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec20c-104">SYNTAX</span></span>

```
Grant-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec20c-105">說明</span><span class="sxs-lookup"><span data-stu-id="ec20c-105">DESCRIPTION</span></span>
<span data-ttu-id="ec20c-106">**Grant AzureRmSnapshotAccess** Cmdlet 會授權存取快照。</span><span class="sxs-lookup"><span data-stu-id="ec20c-106">The **Grant-AzureRmSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="ec20c-107">示例</span><span class="sxs-lookup"><span data-stu-id="ec20c-107">EXAMPLES</span></span>

### <span data-ttu-id="ec20c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ec20c-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="ec20c-109">針對60秒的資源群組中名為「Snapshot01」的快照，授與「Read」的存取權。</span><span class="sxs-lookup"><span data-stu-id="ec20c-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="ec20c-110">參數</span><span class="sxs-lookup"><span data-stu-id="ec20c-110">PARAMETERS</span></span>

### <span data-ttu-id="ec20c-111">-Access</span><span class="sxs-lookup"><span data-stu-id="ec20c-111">-Access</span></span>
<span data-ttu-id="ec20c-112">指定存取層級。</span><span class="sxs-lookup"><span data-stu-id="ec20c-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec20c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec20c-113">-AsJob</span></span>
<span data-ttu-id="ec20c-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ec20c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ec20c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec20c-115">-DefaultProfile</span></span>
<span data-ttu-id="ec20c-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec20c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec20c-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="ec20c-117">-DurationInSecond</span></span>
<span data-ttu-id="ec20c-118">指定存取持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ec20c-118">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec20c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec20c-119">-ResourceGroupName</span></span>
<span data-ttu-id="ec20c-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec20c-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ec20c-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="ec20c-121">-SnapshotName</span></span>
<span data-ttu-id="ec20c-122">指定快照的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec20c-122">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec20c-123">-確認</span><span class="sxs-lookup"><span data-stu-id="ec20c-123">-Confirm</span></span>
<span data-ttu-id="ec20c-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ec20c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec20c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec20c-125">-WhatIf</span></span>
<span data-ttu-id="ec20c-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ec20c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec20c-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec20c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec20c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec20c-128">CommonParameters</span></span>
<span data-ttu-id="ec20c-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec20c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec20c-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ec20c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec20c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="ec20c-131">INPUTS</span></span>

### <span data-ttu-id="ec20c-132">System.object</span><span class="sxs-lookup"><span data-stu-id="ec20c-132">System.String</span></span>

## <span data-ttu-id="ec20c-133">輸出</span><span class="sxs-lookup"><span data-stu-id="ec20c-133">OUTPUTS</span></span>

### <span data-ttu-id="ec20c-134">PSAccessUri 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="ec20c-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="ec20c-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ec20c-135">NOTES</span></span>

## <span data-ttu-id="ec20c-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec20c-136">RELATED LINKS</span></span>