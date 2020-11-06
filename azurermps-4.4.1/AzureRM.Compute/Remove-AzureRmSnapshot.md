---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: 4c7260d3c1131ab573bf933f4b83022cef20819d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456800"
---
# <span data-ttu-id="1c10d-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="1c10d-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="1c10d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c10d-102">SYNOPSIS</span></span>
<span data-ttu-id="1c10d-103">移除快照。</span><span class="sxs-lookup"><span data-stu-id="1c10d-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c10d-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c10d-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c10d-105">說明</span><span class="sxs-lookup"><span data-stu-id="1c10d-105">DESCRIPTION</span></span>
<span data-ttu-id="1c10d-106">**AzureRmSnapshot** Cmdlet 會移除快照。</span><span class="sxs-lookup"><span data-stu-id="1c10d-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="1c10d-107">示例</span><span class="sxs-lookup"><span data-stu-id="1c10d-107">EXAMPLES</span></span>

### <span data-ttu-id="1c10d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1c10d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="1c10d-109">這個命令會移除 [資源] 群組 "ResourceGroup01" 中名為「Snapshot01」的快照。</span><span class="sxs-lookup"><span data-stu-id="1c10d-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="1c10d-110">參數</span><span class="sxs-lookup"><span data-stu-id="1c10d-110">PARAMETERS</span></span>

### <span data-ttu-id="1c10d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c10d-111">-DefaultProfile</span></span>
<span data-ttu-id="1c10d-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c10d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c10d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1c10d-113">-Force</span></span>
<span data-ttu-id="1c10d-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="1c10d-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1c10d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c10d-115">-ResourceGroupName</span></span>
<span data-ttu-id="1c10d-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c10d-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1c10d-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="1c10d-117">-SnapshotName</span></span>
<span data-ttu-id="1c10d-118">指定快照的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c10d-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="1c10d-119">-確認</span><span class="sxs-lookup"><span data-stu-id="1c10d-119">-Confirm</span></span>
<span data-ttu-id="1c10d-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1c10d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c10d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c10d-121">-WhatIf</span></span>
<span data-ttu-id="1c10d-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1c10d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c10d-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1c10d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c10d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c10d-124">CommonParameters</span></span>
<span data-ttu-id="1c10d-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c10d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c10d-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1c10d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c10d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="1c10d-127">INPUTS</span></span>

### <span data-ttu-id="1c10d-128">System.object</span><span class="sxs-lookup"><span data-stu-id="1c10d-128">System.String</span></span>

## <span data-ttu-id="1c10d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="1c10d-129">OUTPUTS</span></span>

### <span data-ttu-id="1c10d-130">System.object</span><span class="sxs-lookup"><span data-stu-id="1c10d-130">System.Object</span></span>

## <span data-ttu-id="1c10d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="1c10d-131">NOTES</span></span>

## <span data-ttu-id="1c10d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c10d-132">RELATED LINKS</span></span>

