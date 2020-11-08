---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: 35e767c340d5418ae500c4cc87a4b40741d8ba6a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958034"
---
# <span data-ttu-id="dab4c-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="dab4c-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="dab4c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dab4c-102">SYNOPSIS</span></span>
<span data-ttu-id="dab4c-103">吊銷快照存取權。</span><span class="sxs-lookup"><span data-stu-id="dab4c-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="dab4c-104">句法</span><span class="sxs-lookup"><span data-stu-id="dab4c-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dab4c-105">說明</span><span class="sxs-lookup"><span data-stu-id="dab4c-105">DESCRIPTION</span></span>
<span data-ttu-id="dab4c-106">**Revoke AzSnapshotAccess** Cmdlet 會吊銷快照的存取權。</span><span class="sxs-lookup"><span data-stu-id="dab4c-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="dab4c-107">示例</span><span class="sxs-lookup"><span data-stu-id="dab4c-107">EXAMPLES</span></span>

### <span data-ttu-id="dab4c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="dab4c-108">Example 1</span></span>
```
PS C:\> Revoke-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="dab4c-109">廢除名為「ResourceGroup01」的資源群組中名為「Snapshot01」的快照存取權</span><span class="sxs-lookup"><span data-stu-id="dab4c-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="dab4c-110">參數</span><span class="sxs-lookup"><span data-stu-id="dab4c-110">PARAMETERS</span></span>

### <span data-ttu-id="dab4c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dab4c-111">-AsJob</span></span>
<span data-ttu-id="dab4c-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dab4c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dab4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dab4c-113">-DefaultProfile</span></span>
<span data-ttu-id="dab4c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dab4c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dab4c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dab4c-115">-ResourceGroupName</span></span>
<span data-ttu-id="dab4c-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dab4c-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="dab4c-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="dab4c-117">-SnapshotName</span></span>
<span data-ttu-id="dab4c-118">指定快照的名稱。</span><span class="sxs-lookup"><span data-stu-id="dab4c-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="dab4c-119">-確認</span><span class="sxs-lookup"><span data-stu-id="dab4c-119">-Confirm</span></span>
<span data-ttu-id="dab4c-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dab4c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dab4c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dab4c-121">-WhatIf</span></span>
<span data-ttu-id="dab4c-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dab4c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dab4c-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dab4c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dab4c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dab4c-124">CommonParameters</span></span>
<span data-ttu-id="dab4c-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dab4c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dab4c-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dab4c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dab4c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="dab4c-127">INPUTS</span></span>

### <span data-ttu-id="dab4c-128">System.object</span><span class="sxs-lookup"><span data-stu-id="dab4c-128">System.String</span></span>

## <span data-ttu-id="dab4c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="dab4c-129">OUTPUTS</span></span>

### <span data-ttu-id="dab4c-130">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="dab4c-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="dab4c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="dab4c-131">NOTES</span></span>

## <span data-ttu-id="dab4c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="dab4c-132">RELATED LINKS</span></span>