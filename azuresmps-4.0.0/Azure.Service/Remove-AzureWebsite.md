---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8062D57E-8381-4715-9AA8-551F15DCC492
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2627bdb2f098d5b09851ec5970dd2a73840d24e6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966929"
---
# <span data-ttu-id="06328-101">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="06328-101">Remove-AzureWebsite</span></span>

## <span data-ttu-id="06328-102">摘要</span><span class="sxs-lookup"><span data-stu-id="06328-102">SYNOPSIS</span></span>
<span data-ttu-id="06328-103">從 Azure 移除指定的網站。</span><span class="sxs-lookup"><span data-stu-id="06328-103">Removes the specified website from Azure.</span></span>

## <span data-ttu-id="06328-104">句法</span><span class="sxs-lookup"><span data-stu-id="06328-104">SYNTAX</span></span>

```
Remove-AzureWebsite [-Force] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06328-105">說明</span><span class="sxs-lookup"><span data-stu-id="06328-105">DESCRIPTION</span></span>
<span data-ttu-id="06328-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06328-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="06328-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="06328-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="06328-108">**AzureWebsite** Cmdlet 會從 Azure 中移除指定的網站，不論是否有確認，都可以使用或不提示進行確認。</span><span class="sxs-lookup"><span data-stu-id="06328-108">The **Remove-AzureWebsite** cmdlet removes the specified website from Azure, either with or without a prompt for confirmation.</span></span>

## <span data-ttu-id="06328-109">示例</span><span class="sxs-lookup"><span data-stu-id="06328-109">EXAMPLES</span></span>

### <span data-ttu-id="06328-110">範例1：移除目前的網站</span><span class="sxs-lookup"><span data-stu-id="06328-110">Example 1: Remove the current website</span></span>
```
PS C:\> Remove-AzureWebsite
```

<span data-ttu-id="06328-111">這個範例會移除與目前目錄相關聯的 Azure 網站。</span><span class="sxs-lookup"><span data-stu-id="06328-111">This example removes the website in Azure associated with the current directory.</span></span>

### <span data-ttu-id="06328-112">範例2：移除網站但不需確認</span><span class="sxs-lookup"><span data-stu-id="06328-112">Example 2: Remove a website without confirmation</span></span>
```
PS C:\> Remove-AzureWebsite -Name mySite -Force
```

<span data-ttu-id="06328-113">這個範例會刪除名為「我的網站」的網站，但不提示您確認。</span><span class="sxs-lookup"><span data-stu-id="06328-113">This example deletes the website named mySite without prompting for confirmation.</span></span>

## <span data-ttu-id="06328-114">參數</span><span class="sxs-lookup"><span data-stu-id="06328-114">PARAMETERS</span></span>

### <span data-ttu-id="06328-115">-Force</span><span class="sxs-lookup"><span data-stu-id="06328-115">-Force</span></span>
<span data-ttu-id="06328-116">如果已指定，則會刪除指定的網站，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="06328-116">If specified, deletes the specified website without prompting for confirmation.</span></span>

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

### <span data-ttu-id="06328-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="06328-117">-Name</span></span>
<span data-ttu-id="06328-118">指定要刪除的網站名稱。</span><span class="sxs-lookup"><span data-stu-id="06328-118">Specifies the name of the website to delete.</span></span>

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

### <span data-ttu-id="06328-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="06328-119">-Profile</span></span>
<span data-ttu-id="06328-120">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="06328-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="06328-121">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="06328-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="06328-122">-槽</span><span class="sxs-lookup"><span data-stu-id="06328-122">-Slot</span></span>
<span data-ttu-id="06328-123">指定網站的槽名稱。</span><span class="sxs-lookup"><span data-stu-id="06328-123">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="06328-124">-確認</span><span class="sxs-lookup"><span data-stu-id="06328-124">-Confirm</span></span>
<span data-ttu-id="06328-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="06328-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06328-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06328-126">-WhatIf</span></span>
<span data-ttu-id="06328-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="06328-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06328-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06328-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06328-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06328-129">CommonParameters</span></span>
<span data-ttu-id="06328-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="06328-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06328-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="06328-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06328-132">輸入</span><span class="sxs-lookup"><span data-stu-id="06328-132">INPUTS</span></span>

## <span data-ttu-id="06328-133">輸出</span><span class="sxs-lookup"><span data-stu-id="06328-133">OUTPUTS</span></span>

## <span data-ttu-id="06328-134">筆記</span><span class="sxs-lookup"><span data-stu-id="06328-134">NOTES</span></span>

## <span data-ttu-id="06328-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="06328-135">RELATED LINKS</span></span>

[<span data-ttu-id="06328-136">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="06328-136">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)


