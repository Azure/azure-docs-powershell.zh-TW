---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermdisk
schema: 2.0.0
ms.openlocfilehash: 5987e92e281dd892ebc56c0a18ca59fc99cfc82d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801734"
---
# <span data-ttu-id="21a41-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="21a41-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="21a41-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21a41-102">SYNOPSIS</span></span>
<span data-ttu-id="21a41-103">移除磁片。</span><span class="sxs-lookup"><span data-stu-id="21a41-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21a41-104">句法</span><span class="sxs-lookup"><span data-stu-id="21a41-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21a41-105">說明</span><span class="sxs-lookup"><span data-stu-id="21a41-105">DESCRIPTION</span></span>
<span data-ttu-id="21a41-106">**AzureRmDisk** Cmdlet 會移除磁片。</span><span class="sxs-lookup"><span data-stu-id="21a41-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="21a41-107">示例</span><span class="sxs-lookup"><span data-stu-id="21a41-107">EXAMPLES</span></span>

### <span data-ttu-id="21a41-108">範例1</span><span class="sxs-lookup"><span data-stu-id="21a41-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="21a41-109">這個命令會移除 [資源] 群組 "ResourceGroup01" 中名為「Disk01」的磁片。</span><span class="sxs-lookup"><span data-stu-id="21a41-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="21a41-110">參數</span><span class="sxs-lookup"><span data-stu-id="21a41-110">PARAMETERS</span></span>

### <span data-ttu-id="21a41-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21a41-111">-AsJob</span></span>
<span data-ttu-id="21a41-112">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="21a41-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="21a41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a41-113">-DefaultProfile</span></span>
<span data-ttu-id="21a41-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21a41-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21a41-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="21a41-115">-DiskName</span></span>
<span data-ttu-id="21a41-116">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="21a41-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="21a41-117">-Force</span><span class="sxs-lookup"><span data-stu-id="21a41-117">-Force</span></span>
<span data-ttu-id="21a41-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="21a41-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="21a41-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21a41-119">-ResourceGroupName</span></span>
<span data-ttu-id="21a41-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="21a41-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="21a41-121">-確認</span><span class="sxs-lookup"><span data-stu-id="21a41-121">-Confirm</span></span>
<span data-ttu-id="21a41-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="21a41-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21a41-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21a41-123">-WhatIf</span></span>
<span data-ttu-id="21a41-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="21a41-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21a41-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21a41-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21a41-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a41-126">CommonParameters</span></span>
<span data-ttu-id="21a41-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21a41-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a41-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="21a41-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a41-129">輸入</span><span class="sxs-lookup"><span data-stu-id="21a41-129">INPUTS</span></span>

### <span data-ttu-id="21a41-130">System.object</span><span class="sxs-lookup"><span data-stu-id="21a41-130">System.String</span></span>

## <span data-ttu-id="21a41-131">輸出</span><span class="sxs-lookup"><span data-stu-id="21a41-131">OUTPUTS</span></span>

### <span data-ttu-id="21a41-132">System.object</span><span class="sxs-lookup"><span data-stu-id="21a41-132">System.Object</span></span>

## <span data-ttu-id="21a41-133">筆記</span><span class="sxs-lookup"><span data-stu-id="21a41-133">NOTES</span></span>

## <span data-ttu-id="21a41-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="21a41-134">RELATED LINKS</span></span>

