---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 756F757C-8CDE-43A5-A8A6-D55EF9C66183
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71402e56251e2632c73a9185a1e70b4e3de8d770
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967447"
---
# <span data-ttu-id="04d3b-101">New-AzureMediaServicesKey</span><span class="sxs-lookup"><span data-stu-id="04d3b-101">New-AzureMediaServicesKey</span></span>

## <span data-ttu-id="04d3b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="04d3b-103">更新 Azure 媒體服務帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="04d3b-103">Updates Azure Media Services account keys.</span></span>

<span data-ttu-id="04d3b-104">**注意：** 此版本已棄用，請參閱 [較新的版本](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services)。</span><span class="sxs-lookup"><span data-stu-id="04d3b-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="04d3b-105">句法</span><span class="sxs-lookup"><span data-stu-id="04d3b-105">SYNTAX</span></span>

```
New-AzureMediaServicesKey -Name <String> -KeyType <MediaServicesKeyType> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04d3b-106">說明</span><span class="sxs-lookup"><span data-stu-id="04d3b-106">DESCRIPTION</span></span>
<span data-ttu-id="04d3b-107">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04d3b-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="04d3b-108">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="04d3b-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="04d3b-109">**新的-AzureMediaServicesKey** Cmdlet 會更新指定媒體服務帳戶的主要或次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="04d3b-109">The **New-AzureMediaServicesKey** cmdlet updates the Primary or Secondary key for the specified Media Services account.</span></span>

## <span data-ttu-id="04d3b-110">示例</span><span class="sxs-lookup"><span data-stu-id="04d3b-110">EXAMPLES</span></span>

### <span data-ttu-id="04d3b-111">範例1：更新媒體服務帳戶金鑰</span><span class="sxs-lookup"><span data-stu-id="04d3b-111">Example 1: Update a Media Services account key</span></span>
```
PS C:\> New-AzureMediaServicesKey -Name "mediaservicesaccount" -KeyType "Primary" -Force
```

## <span data-ttu-id="04d3b-112">參數</span><span class="sxs-lookup"><span data-stu-id="04d3b-112">PARAMETERS</span></span>

### <span data-ttu-id="04d3b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="04d3b-113">-Force</span></span>
<span data-ttu-id="04d3b-114">表示未確認金鑰產生。</span><span class="sxs-lookup"><span data-stu-id="04d3b-114">Indicates that the key generation is not confirmed.</span></span>

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

### <span data-ttu-id="04d3b-115">-KeyType</span><span class="sxs-lookup"><span data-stu-id="04d3b-115">-KeyType</span></span>
<span data-ttu-id="04d3b-116">指定媒體服務金鑰類型;有效值為：</span><span class="sxs-lookup"><span data-stu-id="04d3b-116">Specifies the Media Services key type; Valid values are:</span></span>
  
- <span data-ttu-id="04d3b-117">首選</span><span class="sxs-lookup"><span data-stu-id="04d3b-117">Primary</span></span>
- <span data-ttu-id="04d3b-118">備用</span><span class="sxs-lookup"><span data-stu-id="04d3b-118">Secondary</span></span>

```yaml
Type: MediaServicesKeyType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04d3b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="04d3b-119">-Name</span></span>
<span data-ttu-id="04d3b-120">指定媒體服務帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="04d3b-120">Specifies the name of the Media Services account.</span></span>

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

### <span data-ttu-id="04d3b-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="04d3b-121">-Profile</span></span>
<span data-ttu-id="04d3b-122">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="04d3b-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="04d3b-123">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="04d3b-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="04d3b-124">-確認</span><span class="sxs-lookup"><span data-stu-id="04d3b-124">-Confirm</span></span>
<span data-ttu-id="04d3b-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="04d3b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04d3b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04d3b-126">-WhatIf</span></span>
<span data-ttu-id="04d3b-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="04d3b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04d3b-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04d3b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04d3b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04d3b-129">CommonParameters</span></span>
<span data-ttu-id="04d3b-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04d3b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04d3b-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="04d3b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04d3b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="04d3b-132">INPUTS</span></span>

## <span data-ttu-id="04d3b-133">輸出</span><span class="sxs-lookup"><span data-stu-id="04d3b-133">OUTPUTS</span></span>

## <span data-ttu-id="04d3b-134">筆記</span><span class="sxs-lookup"><span data-stu-id="04d3b-134">NOTES</span></span>

## <span data-ttu-id="04d3b-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="04d3b-135">RELATED LINKS</span></span>

[<span data-ttu-id="04d3b-136">如何使用 Azure PowerShell for 媒體服務</span><span class="sxs-lookup"><span data-stu-id="04d3b-136">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)


