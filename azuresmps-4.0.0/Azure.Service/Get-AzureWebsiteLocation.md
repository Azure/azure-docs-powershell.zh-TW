---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6313BAB9-32D1-4B4B-A0C7-345F20629505
online version: ''
schema: 2.0.0
ms.openlocfilehash: 73b461bb5dfd70576079d333366c50f5e6f56900
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967718"
---
# <span data-ttu-id="3b353-101">Get-AzureWebsiteLocation</span><span class="sxs-lookup"><span data-stu-id="3b353-101">Get-AzureWebsiteLocation</span></span>

## <span data-ttu-id="3b353-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b353-102">SYNOPSIS</span></span>
<span data-ttu-id="3b353-103">取得所有可用的網站位置。</span><span class="sxs-lookup"><span data-stu-id="3b353-103">Gets all available website locations.</span></span>

## <span data-ttu-id="3b353-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b353-104">SYNTAX</span></span>

```
Get-AzureWebsiteLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3b353-105">說明</span><span class="sxs-lookup"><span data-stu-id="3b353-105">DESCRIPTION</span></span>
<span data-ttu-id="3b353-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b353-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3b353-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="3b353-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3b353-108">取得目前訂閱的所有可用網站位置</span><span class="sxs-lookup"><span data-stu-id="3b353-108">Gets all of the available website locations for the current subscription</span></span>

## <span data-ttu-id="3b353-109">示例</span><span class="sxs-lookup"><span data-stu-id="3b353-109">EXAMPLES</span></span>

### <span data-ttu-id="3b353-110">範例1：取得所有可用的位置</span><span class="sxs-lookup"><span data-stu-id="3b353-110">Example 1: Get all available locations</span></span>
```
PS C:\> Get-AzureWebsiteLocations
```

<span data-ttu-id="3b353-111">這個範例會取得目前訂閱的所有可用網站位置。</span><span class="sxs-lookup"><span data-stu-id="3b353-111">This example gets all of the available website locations for the current subscription.</span></span>

## <span data-ttu-id="3b353-112">參數</span><span class="sxs-lookup"><span data-stu-id="3b353-112">PARAMETERS</span></span>

### <span data-ttu-id="3b353-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3b353-113">-Profile</span></span>
<span data-ttu-id="3b353-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3b353-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3b353-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="3b353-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3b353-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b353-116">CommonParameters</span></span>
<span data-ttu-id="3b353-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b353-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b353-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3b353-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b353-119">輸入</span><span class="sxs-lookup"><span data-stu-id="3b353-119">INPUTS</span></span>

## <span data-ttu-id="3b353-120">輸出</span><span class="sxs-lookup"><span data-stu-id="3b353-120">OUTPUTS</span></span>

## <span data-ttu-id="3b353-121">筆記</span><span class="sxs-lookup"><span data-stu-id="3b353-121">NOTES</span></span>

## <span data-ttu-id="3b353-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b353-122">RELATED LINKS</span></span>

[<span data-ttu-id="3b353-123">新-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="3b353-123">New-AzureWebsite</span></span>](./New-AzureWebsite.md)


