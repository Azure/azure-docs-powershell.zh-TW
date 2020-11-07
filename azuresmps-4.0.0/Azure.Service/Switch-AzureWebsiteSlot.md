---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 496ABC97-A493-4E42-B998-28A907DFBC19
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0641fd7bc8dcfa5048ac3e9d922bade199af2bab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967385"
---
# <span data-ttu-id="b82bb-101">Switch-AzureWebsiteSlot</span><span class="sxs-lookup"><span data-stu-id="b82bb-101">Switch-AzureWebsiteSlot</span></span>

## <span data-ttu-id="b82bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b82bb-102">SYNOPSIS</span></span>
<span data-ttu-id="b82bb-103">將有其他槽的網站的生產槽交換。</span><span class="sxs-lookup"><span data-stu-id="b82bb-103">Swaps the production slot for a website with another slot.</span></span>

## <span data-ttu-id="b82bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="b82bb-104">SYNTAX</span></span>

```
Switch-AzureWebsiteSlot [-Name <String>] [-Slot1 <String>] [-Slot2 <String>] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b82bb-105">說明</span><span class="sxs-lookup"><span data-stu-id="b82bb-105">DESCRIPTION</span></span>
<span data-ttu-id="b82bb-106">**AzureWebsiteSlot** Cmdlet 會將網站的生產槽換成其他槽。</span><span class="sxs-lookup"><span data-stu-id="b82bb-106">The **Switch-AzureWebsiteSlot** cmdlet swaps the production slot for a website with another slot.</span></span>
<span data-ttu-id="b82bb-107">這適用于只有兩個槽的網站。</span><span class="sxs-lookup"><span data-stu-id="b82bb-107">This works on websites with two slots only.</span></span>

## <span data-ttu-id="b82bb-108">示例</span><span class="sxs-lookup"><span data-stu-id="b82bb-108">EXAMPLES</span></span>

### <span data-ttu-id="b82bb-109">範例1：切換網站槽</span><span class="sxs-lookup"><span data-stu-id="b82bb-109">Example 1: Switch Website Slot</span></span>
```
PS C:\> Switch-AzureWebsiteSlot -Name MyWebsite
```

<span data-ttu-id="b82bb-110">使用生產槽切換 azure 網站 MyWebsite 備份槽。</span><span class="sxs-lookup"><span data-stu-id="b82bb-110">Switch the azure website MyWebsite backup slot with production slot.</span></span>

## <span data-ttu-id="b82bb-111">參數</span><span class="sxs-lookup"><span data-stu-id="b82bb-111">PARAMETERS</span></span>

### <span data-ttu-id="b82bb-112">-Force</span><span class="sxs-lookup"><span data-stu-id="b82bb-112">-Force</span></span>
<span data-ttu-id="b82bb-113">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b82bb-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b82bb-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="b82bb-114">-Name</span></span>
<span data-ttu-id="b82bb-115">網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="b82bb-115">The name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b82bb-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b82bb-116">-Profile</span></span>
<span data-ttu-id="b82bb-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b82bb-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b82bb-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b82bb-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b82bb-119">-Slot1</span><span class="sxs-lookup"><span data-stu-id="b82bb-119">-Slot1</span></span>
<span data-ttu-id="b82bb-120">指定第一個槽。</span><span class="sxs-lookup"><span data-stu-id="b82bb-120">Specifies the first slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b82bb-121">-Slot2</span><span class="sxs-lookup"><span data-stu-id="b82bb-121">-Slot2</span></span>
<span data-ttu-id="b82bb-122">指定第二個槽。</span><span class="sxs-lookup"><span data-stu-id="b82bb-122">Specifies the second slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b82bb-123">-確認</span><span class="sxs-lookup"><span data-stu-id="b82bb-123">-Confirm</span></span>
<span data-ttu-id="b82bb-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b82bb-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b82bb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b82bb-125">-WhatIf</span></span>
<span data-ttu-id="b82bb-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b82bb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b82bb-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b82bb-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b82bb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b82bb-128">CommonParameters</span></span>
<span data-ttu-id="b82bb-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b82bb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b82bb-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b82bb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b82bb-131">輸入</span><span class="sxs-lookup"><span data-stu-id="b82bb-131">INPUTS</span></span>

## <span data-ttu-id="b82bb-132">輸出</span><span class="sxs-lookup"><span data-stu-id="b82bb-132">OUTPUTS</span></span>

## <span data-ttu-id="b82bb-133">筆記</span><span class="sxs-lookup"><span data-stu-id="b82bb-133">NOTES</span></span>

## <span data-ttu-id="b82bb-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="b82bb-134">RELATED LINKS</span></span>

[<span data-ttu-id="b82bb-135">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b82bb-135">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="b82bb-136">新-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b82bb-136">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="b82bb-137">開始-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b82bb-137">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="b82bb-138">停止 AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b82bb-138">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


