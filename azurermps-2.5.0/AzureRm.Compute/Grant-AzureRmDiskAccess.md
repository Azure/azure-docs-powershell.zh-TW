---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/grant-azurermdiskaccess
schema: 2.0.0
ms.openlocfilehash: c574b273082d3c7e840d589fe765190d99028d89
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801421"
---
# <span data-ttu-id="9b5cc-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="9b5cc-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="9b5cc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b5cc-102">SYNOPSIS</span></span>
<span data-ttu-id="9b5cc-103">授權存取磁片。</span><span class="sxs-lookup"><span data-stu-id="9b5cc-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b5cc-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b5cc-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-Access] <AccessLevel>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b5cc-105">說明</span><span class="sxs-lookup"><span data-stu-id="9b5cc-105">DESCRIPTION</span></span>
<span data-ttu-id="9b5cc-106">**Grant AzureRmDiskAccess** Cmdlet 可授權存取磁片。</span><span class="sxs-lookup"><span data-stu-id="9b5cc-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="9b5cc-107">示例</span><span class="sxs-lookup"><span data-stu-id="9b5cc-107">EXAMPLES</span></span>

### <span data-ttu-id="9b5cc-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9b5cc-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="9b5cc-109">針對60秒的資源群組中名為 "Disk01" 的磁片，授與「Read」的存取權。</span><span class="sxs-lookup"><span data-stu-id="9b5cc-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="9b5cc-110">參數</span><span class="sxs-lookup"><span data-stu-id="9b5cc-110">PARAMETERS</span></span>

### <span data-ttu-id="9b5cc-111">-Access</span><span class="sxs-lookup"><span data-stu-id="9b5cc-111">-Access</span></span>
<span data-ttu-id="9b5cc-112">指定存取層級。</span><span class="sxs-lookup"><span data-stu-id="9b5cc-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="9b5cc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b5cc-113">-AsJob</span></span>
<span data-ttu-id="9b5cc-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9b5cc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b5cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b5cc-115">-DefaultProfile</span></span>
<span data-ttu-id="9b5cc-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b5cc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b5cc-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="9b5cc-117">-DiskName</span></span>
<span data-ttu-id="9b5cc-118">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b5cc-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="9b5cc-119">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="9b5cc-119">-DurationInSecond</span></span>
<span data-ttu-id="9b5cc-120">指定存取持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="9b5cc-120">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="9b5cc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b5cc-121">-ResourceGroupName</span></span>
<span data-ttu-id="9b5cc-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b5cc-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9b5cc-123">-確認</span><span class="sxs-lookup"><span data-stu-id="9b5cc-123">-Confirm</span></span>
<span data-ttu-id="9b5cc-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9b5cc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b5cc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b5cc-125">-WhatIf</span></span>
<span data-ttu-id="9b5cc-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9b5cc-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b5cc-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9b5cc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b5cc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b5cc-128">CommonParameters</span></span>
<span data-ttu-id="9b5cc-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b5cc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b5cc-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9b5cc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b5cc-131">輸入</span><span class="sxs-lookup"><span data-stu-id="9b5cc-131">INPUTS</span></span>

### <span data-ttu-id="9b5cc-132">System.object</span><span class="sxs-lookup"><span data-stu-id="9b5cc-132">System.String</span></span>

## <span data-ttu-id="9b5cc-133">輸出</span><span class="sxs-lookup"><span data-stu-id="9b5cc-133">OUTPUTS</span></span>

### <span data-ttu-id="9b5cc-134">System.object</span><span class="sxs-lookup"><span data-stu-id="9b5cc-134">System.Object</span></span>

## <span data-ttu-id="9b5cc-135">筆記</span><span class="sxs-lookup"><span data-stu-id="9b5cc-135">NOTES</span></span>

## <span data-ttu-id="9b5cc-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b5cc-136">RELATED LINKS</span></span>

