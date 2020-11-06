---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: edd2d89cfe0488021ef62780ade80cb2b98437c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445672"
---
# <span data-ttu-id="4486c-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="4486c-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="4486c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4486c-102">SYNOPSIS</span></span>
<span data-ttu-id="4486c-103">移除快照。</span><span class="sxs-lookup"><span data-stu-id="4486c-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4486c-104">句法</span><span class="sxs-lookup"><span data-stu-id="4486c-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4486c-105">說明</span><span class="sxs-lookup"><span data-stu-id="4486c-105">DESCRIPTION</span></span>
<span data-ttu-id="4486c-106">**AzureRmSnapshot** Cmdlet 會移除快照。</span><span class="sxs-lookup"><span data-stu-id="4486c-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="4486c-107">示例</span><span class="sxs-lookup"><span data-stu-id="4486c-107">EXAMPLES</span></span>

### <span data-ttu-id="4486c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4486c-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="4486c-109">這個命令會移除 [資源] 群組 "ResourceGroup01" 中名為「Snapshot01」的快照。</span><span class="sxs-lookup"><span data-stu-id="4486c-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4486c-110">參數</span><span class="sxs-lookup"><span data-stu-id="4486c-110">PARAMETERS</span></span>

### <span data-ttu-id="4486c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4486c-111">-AsJob</span></span>
<span data-ttu-id="4486c-112">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="4486c-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4486c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4486c-113">-DefaultProfile</span></span>
<span data-ttu-id="4486c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4486c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4486c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4486c-115">-Force</span></span>
<span data-ttu-id="4486c-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="4486c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4486c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4486c-117">-ResourceGroupName</span></span>
<span data-ttu-id="4486c-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4486c-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4486c-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="4486c-119">-SnapshotName</span></span>
<span data-ttu-id="4486c-120">指定快照的名稱。</span><span class="sxs-lookup"><span data-stu-id="4486c-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="4486c-121">-確認</span><span class="sxs-lookup"><span data-stu-id="4486c-121">-Confirm</span></span>
<span data-ttu-id="4486c-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4486c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4486c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4486c-123">-WhatIf</span></span>
<span data-ttu-id="4486c-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4486c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4486c-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4486c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4486c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4486c-126">CommonParameters</span></span>
<span data-ttu-id="4486c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4486c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4486c-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4486c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4486c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="4486c-129">INPUTS</span></span>

### <span data-ttu-id="4486c-130">System.object</span><span class="sxs-lookup"><span data-stu-id="4486c-130">System.String</span></span>

## <span data-ttu-id="4486c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="4486c-131">OUTPUTS</span></span>

### <span data-ttu-id="4486c-132">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="4486c-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4486c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="4486c-133">NOTES</span></span>

## <span data-ttu-id="4486c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="4486c-134">RELATED LINKS</span></span>
