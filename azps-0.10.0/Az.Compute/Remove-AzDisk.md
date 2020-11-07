---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: 9e3a194d1143134b1ba3aa472db61062baf847f1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796070"
---
# <span data-ttu-id="4d8a4-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="4d8a4-101">Remove-AzDisk</span></span>

## <span data-ttu-id="4d8a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4d8a4-102">SYNOPSIS</span></span>
<span data-ttu-id="4d8a4-103">移除磁片。</span><span class="sxs-lookup"><span data-stu-id="4d8a4-103">Removes a disk.</span></span>

## <span data-ttu-id="4d8a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="4d8a4-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d8a4-105">說明</span><span class="sxs-lookup"><span data-stu-id="4d8a4-105">DESCRIPTION</span></span>
<span data-ttu-id="4d8a4-106">**AzDisk** Cmdlet 會移除磁片。</span><span class="sxs-lookup"><span data-stu-id="4d8a4-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="4d8a4-107">示例</span><span class="sxs-lookup"><span data-stu-id="4d8a4-107">EXAMPLES</span></span>

### <span data-ttu-id="4d8a4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4d8a4-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="4d8a4-109">這個命令會移除 [資源] 群組 "ResourceGroup01" 中名為「Disk01」的磁片。</span><span class="sxs-lookup"><span data-stu-id="4d8a4-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="4d8a4-110">參數</span><span class="sxs-lookup"><span data-stu-id="4d8a4-110">PARAMETERS</span></span>

### <span data-ttu-id="4d8a4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d8a4-111">-AsJob</span></span>
<span data-ttu-id="4d8a4-112">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="4d8a4-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4d8a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d8a4-113">-DefaultProfile</span></span>
<span data-ttu-id="4d8a4-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4d8a4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d8a4-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="4d8a4-115">-DiskName</span></span>
<span data-ttu-id="4d8a4-116">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d8a4-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="4d8a4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4d8a4-117">-Force</span></span>
<span data-ttu-id="4d8a4-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="4d8a4-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4d8a4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d8a4-119">-ResourceGroupName</span></span>
<span data-ttu-id="4d8a4-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d8a4-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4d8a4-121">-確認</span><span class="sxs-lookup"><span data-stu-id="4d8a4-121">-Confirm</span></span>
<span data-ttu-id="4d8a4-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4d8a4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d8a4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d8a4-123">-WhatIf</span></span>
<span data-ttu-id="4d8a4-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4d8a4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d8a4-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4d8a4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d8a4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d8a4-126">CommonParameters</span></span>
<span data-ttu-id="4d8a4-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4d8a4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d8a4-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4d8a4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d8a4-129">輸入</span><span class="sxs-lookup"><span data-stu-id="4d8a4-129">INPUTS</span></span>

### <span data-ttu-id="4d8a4-130">System.object</span><span class="sxs-lookup"><span data-stu-id="4d8a4-130">System.String</span></span>

## <span data-ttu-id="4d8a4-131">輸出</span><span class="sxs-lookup"><span data-stu-id="4d8a4-131">OUTPUTS</span></span>

### <span data-ttu-id="4d8a4-132">System.object</span><span class="sxs-lookup"><span data-stu-id="4d8a4-132">System.Object</span></span>

## <span data-ttu-id="4d8a4-133">筆記</span><span class="sxs-lookup"><span data-stu-id="4d8a4-133">NOTES</span></span>

## <span data-ttu-id="4d8a4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="4d8a4-134">RELATED LINKS</span></span>

