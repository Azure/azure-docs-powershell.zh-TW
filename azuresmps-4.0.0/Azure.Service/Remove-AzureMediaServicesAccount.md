---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5B255D11-0A9B-4679-A2AC-4357B293EE96
online version: ''
schema: 2.0.0
ms.openlocfilehash: e4eee130312ae52e95b020151750d46144bc3685
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967917"
---
# <span data-ttu-id="6c3e3-101">Remove-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6c3e3-101">Remove-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="6c3e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c3e3-102">SYNOPSIS</span></span>
<span data-ttu-id="6c3e3-103">移除指定的 Azure 媒體服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="6c3e3-103">Removes the specified Azure Media Services account.</span></span>

<span data-ttu-id="6c3e3-104">**注意：**  此版本已棄用，請參閱 [較新的版本](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services)。</span><span class="sxs-lookup"><span data-stu-id="6c3e3-104">**Note:**  This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="6c3e3-105">句法</span><span class="sxs-lookup"><span data-stu-id="6c3e3-105">SYNTAX</span></span>

```
Remove-AzureMediaServicesAccount -Name <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c3e3-106">說明</span><span class="sxs-lookup"><span data-stu-id="6c3e3-106">DESCRIPTION</span></span>
<span data-ttu-id="6c3e3-107">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c3e3-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6c3e3-108">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="6c3e3-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6c3e3-109">**AzureMediaServicesAccount** Cmdlet 會移除媒體服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="6c3e3-109">The **Remove-AzureMediaServicesAccount** cmdlet removes a Media Services account.</span></span>

## <span data-ttu-id="6c3e3-110">示例</span><span class="sxs-lookup"><span data-stu-id="6c3e3-110">EXAMPLES</span></span>

### <span data-ttu-id="6c3e3-111">範例1：刪除媒體服務帳戶</span><span class="sxs-lookup"><span data-stu-id="6c3e3-111">Example 1: Delete a Media Services account</span></span>
```
PS C:\> Remove-AzureMediaServicesAccount -Name "mediaservicesaccount" -Force
```

## <span data-ttu-id="6c3e3-112">參數</span><span class="sxs-lookup"><span data-stu-id="6c3e3-112">PARAMETERS</span></span>

### <span data-ttu-id="6c3e3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6c3e3-113">-Force</span></span>
<span data-ttu-id="6c3e3-114">如果指定了 *Force* 開關，就不會確認刪除。</span><span class="sxs-lookup"><span data-stu-id="6c3e3-114">If the *Force* switch is specified, the deletion is not confirmed.</span></span>

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

### <span data-ttu-id="6c3e3-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c3e3-115">-Name</span></span>
<span data-ttu-id="6c3e3-116">媒體服務帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="6c3e3-116">The Media Services account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c3e3-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="6c3e3-117">-Profile</span></span>
<span data-ttu-id="6c3e3-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="6c3e3-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6c3e3-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="6c3e3-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6c3e3-120">-確認</span><span class="sxs-lookup"><span data-stu-id="6c3e3-120">-Confirm</span></span>
<span data-ttu-id="6c3e3-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6c3e3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c3e3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c3e3-122">-WhatIf</span></span>
<span data-ttu-id="6c3e3-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6c3e3-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c3e3-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c3e3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c3e3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c3e3-125">CommonParameters</span></span>
<span data-ttu-id="6c3e3-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c3e3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c3e3-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6c3e3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c3e3-128">輸入</span><span class="sxs-lookup"><span data-stu-id="6c3e3-128">INPUTS</span></span>

## <span data-ttu-id="6c3e3-129">輸出</span><span class="sxs-lookup"><span data-stu-id="6c3e3-129">OUTPUTS</span></span>

## <span data-ttu-id="6c3e3-130">筆記</span><span class="sxs-lookup"><span data-stu-id="6c3e3-130">NOTES</span></span>

## <span data-ttu-id="6c3e3-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c3e3-131">RELATED LINKS</span></span>

[<span data-ttu-id="6c3e3-132">如何使用 Azure PowerShell for 媒體服務</span><span class="sxs-lookup"><span data-stu-id="6c3e3-132">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)

[<span data-ttu-id="6c3e3-133">AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6c3e3-133">Get-AzureMediaServicesAccount</span></span>](./Get-AzureMediaServicesAccount.md)

[<span data-ttu-id="6c3e3-134">新-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="6c3e3-134">New-AzureMediaServicesAccount</span></span>](./New-AzureMediaServicesAccount.md)


