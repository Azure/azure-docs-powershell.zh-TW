---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzDiskAccess.md
ms.openlocfilehash: 39565aa0675a0afc5f6f3996cad522b435a1a9b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143395"
---
# <span data-ttu-id="70167-101">Grant-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="70167-101">Grant-AzDiskAccess</span></span>

## <span data-ttu-id="70167-102">摘要</span><span class="sxs-lookup"><span data-stu-id="70167-102">SYNOPSIS</span></span>
<span data-ttu-id="70167-103">授權存取磁片。</span><span class="sxs-lookup"><span data-stu-id="70167-103">Grants an access to a disk.</span></span>

## <span data-ttu-id="70167-104">句法</span><span class="sxs-lookup"><span data-stu-id="70167-104">SYNTAX</span></span>

```
Grant-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70167-105">說明</span><span class="sxs-lookup"><span data-stu-id="70167-105">DESCRIPTION</span></span>
<span data-ttu-id="70167-106">**Grant AzDiskAccess** Cmdlet 可授權存取磁片。</span><span class="sxs-lookup"><span data-stu-id="70167-106">The **Grant-AzDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="70167-107">示例</span><span class="sxs-lookup"><span data-stu-id="70167-107">EXAMPLES</span></span>

### <span data-ttu-id="70167-108">範例1</span><span class="sxs-lookup"><span data-stu-id="70167-108">Example 1</span></span>
```
PS C:\> Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="70167-109">針對60秒的資源群組中名為 "Disk01" 的磁片，授與「Read」的存取權。</span><span class="sxs-lookup"><span data-stu-id="70167-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="70167-110">參數</span><span class="sxs-lookup"><span data-stu-id="70167-110">PARAMETERS</span></span>

### <span data-ttu-id="70167-111">-Access</span><span class="sxs-lookup"><span data-stu-id="70167-111">-Access</span></span>
<span data-ttu-id="70167-112">指定存取層級。</span><span class="sxs-lookup"><span data-stu-id="70167-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="70167-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70167-113">-AsJob</span></span>
<span data-ttu-id="70167-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="70167-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70167-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70167-115">-DefaultProfile</span></span>
<span data-ttu-id="70167-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="70167-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70167-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="70167-117">-DiskName</span></span>
<span data-ttu-id="70167-118">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="70167-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="70167-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="70167-119">-DurationInSecond</span></span>
<span data-ttu-id="70167-120">指定存取持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="70167-120">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="70167-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70167-121">-ResourceGroupName</span></span>
<span data-ttu-id="70167-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="70167-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="70167-123">-確認</span><span class="sxs-lookup"><span data-stu-id="70167-123">-Confirm</span></span>
<span data-ttu-id="70167-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="70167-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70167-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70167-125">-WhatIf</span></span>
<span data-ttu-id="70167-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="70167-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70167-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="70167-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70167-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70167-128">CommonParameters</span></span>
<span data-ttu-id="70167-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="70167-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70167-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="70167-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70167-131">輸入</span><span class="sxs-lookup"><span data-stu-id="70167-131">INPUTS</span></span>

### <span data-ttu-id="70167-132">System.object</span><span class="sxs-lookup"><span data-stu-id="70167-132">System.String</span></span>

## <span data-ttu-id="70167-133">輸出</span><span class="sxs-lookup"><span data-stu-id="70167-133">OUTPUTS</span></span>

### <span data-ttu-id="70167-134">PSAccessUri 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="70167-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="70167-135">筆記</span><span class="sxs-lookup"><span data-stu-id="70167-135">NOTES</span></span>

## <span data-ttu-id="70167-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="70167-136">RELATED LINKS</span></span>
