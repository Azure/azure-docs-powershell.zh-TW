---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: b18db3b4e8448212b413dc13887ea68b35f22422
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902121"
---
# <span data-ttu-id="40629-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="40629-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="40629-102">簡介</span><span class="sxs-lookup"><span data-stu-id="40629-102">SYNOPSIS</span></span>
<span data-ttu-id="40629-103">撤銷快照的存取權。</span><span class="sxs-lookup"><span data-stu-id="40629-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="40629-104">語法</span><span class="sxs-lookup"><span data-stu-id="40629-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40629-105">描述</span><span class="sxs-lookup"><span data-stu-id="40629-105">DESCRIPTION</span></span>
<span data-ttu-id="40629-106">**Revoke-AzSnapshotAccess** Cmdlet 會撤銷快照的存取權。</span><span class="sxs-lookup"><span data-stu-id="40629-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="40629-107">例子</span><span class="sxs-lookup"><span data-stu-id="40629-107">EXAMPLES</span></span>

### <span data-ttu-id="40629-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="40629-108">Example 1</span></span>
```
PS C:\> Revoke-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="40629-109">撤銷名稱為 "ResourceGroup01" 的資源群組中名為 "Snapshot01" 的快照存取權</span><span class="sxs-lookup"><span data-stu-id="40629-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="40629-110">參數</span><span class="sxs-lookup"><span data-stu-id="40629-110">PARAMETERS</span></span>

### <span data-ttu-id="40629-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40629-111">-AsJob</span></span>
<span data-ttu-id="40629-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="40629-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="40629-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40629-113">-DefaultProfile</span></span>
<span data-ttu-id="40629-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="40629-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40629-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40629-115">-ResourceGroupName</span></span>
<span data-ttu-id="40629-116">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="40629-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="40629-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="40629-117">-SnapshotName</span></span>
<span data-ttu-id="40629-118">指定快照名稱。</span><span class="sxs-lookup"><span data-stu-id="40629-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="40629-119">-確認</span><span class="sxs-lookup"><span data-stu-id="40629-119">-Confirm</span></span>
<span data-ttu-id="40629-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="40629-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40629-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40629-121">-WhatIf</span></span>
<span data-ttu-id="40629-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="40629-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40629-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40629-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40629-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40629-124">CommonParameters</span></span>
<span data-ttu-id="40629-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="40629-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40629-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40629-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40629-127">輸入</span><span class="sxs-lookup"><span data-stu-id="40629-127">INPUTS</span></span>

### <span data-ttu-id="40629-128">System.String</span><span class="sxs-lookup"><span data-stu-id="40629-128">System.String</span></span>

## <span data-ttu-id="40629-129">輸出</span><span class="sxs-lookup"><span data-stu-id="40629-129">OUTPUTS</span></span>

### <span data-ttu-id="40629-130">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="40629-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="40629-131">筆記</span><span class="sxs-lookup"><span data-stu-id="40629-131">NOTES</span></span>

## <span data-ttu-id="40629-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="40629-132">RELATED LINKS</span></span>
