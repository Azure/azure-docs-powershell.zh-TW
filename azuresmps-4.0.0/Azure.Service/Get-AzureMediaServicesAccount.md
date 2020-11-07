---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1327796-0CDC-43E0-97A6-FD1BF570066F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c8676fbf957ebe96f0e849eedd3f64aca19a7741
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967781"
---
# <span data-ttu-id="74091-101">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="74091-101">Get-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="74091-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74091-102">SYNOPSIS</span></span>
<span data-ttu-id="74091-103">取得可用的 Azure 媒體服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="74091-103">Gets the available Azure Media Services accounts.</span></span>

<span data-ttu-id="74091-104">**注意：** 此版本已棄用，請參閱 [較新的版本](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services)。</span><span class="sxs-lookup"><span data-stu-id="74091-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="74091-105">句法</span><span class="sxs-lookup"><span data-stu-id="74091-105">SYNTAX</span></span>

```
Get-AzureMediaServicesAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="74091-106">說明</span><span class="sxs-lookup"><span data-stu-id="74091-106">DESCRIPTION</span></span>
<span data-ttu-id="74091-107">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74091-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="74091-108">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="74091-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="74091-109">若要列出所有帳戶，請使用 `Get-AzureMediaServicesAccount` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74091-109">To list all the accounts, use the `Get-AzureMediaServicesAccount` cmdlet.</span></span>
<span data-ttu-id="74091-110">若要取得特定帳戶的詳細資訊，請使用 `Get-AzureMediaServicesAccount -Name YourAccountName` Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74091-110">To get more detailed information about a specific account, use the `Get-AzureMediaServicesAccount -Name YourAccountName` cmdlet.</span></span>

## <span data-ttu-id="74091-111">示例</span><span class="sxs-lookup"><span data-stu-id="74091-111">EXAMPLES</span></span>

### <span data-ttu-id="74091-112">範例1：列出所有媒體服務帳戶</span><span class="sxs-lookup"><span data-stu-id="74091-112">Example 1: List all Media Services accounts</span></span>
```
PS C:\> Get-AzureMediaServicesAccount
```

<span data-ttu-id="74091-113">這個命令會列出所有可用的媒體服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="74091-113">This command lists all available Media Services accounts.</span></span>

### <span data-ttu-id="74091-114">範例2：取得媒體服務帳戶的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="74091-114">Example 2: Get detailed information about a Media Services account</span></span>
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

<span data-ttu-id="74091-115">這個命令會顯示媒體服務帳戶的屬性。</span><span class="sxs-lookup"><span data-stu-id="74091-115">This command displays properties of a Media Services account.</span></span>

## <span data-ttu-id="74091-116">參數</span><span class="sxs-lookup"><span data-stu-id="74091-116">PARAMETERS</span></span>

### <span data-ttu-id="74091-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="74091-117">-Name</span></span>
<span data-ttu-id="74091-118">媒體服務帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="74091-118">The Media Services account name.</span></span>

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

### <span data-ttu-id="74091-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="74091-119">-Profile</span></span>
<span data-ttu-id="74091-120">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="74091-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="74091-121">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="74091-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="74091-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74091-122">CommonParameters</span></span>
<span data-ttu-id="74091-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74091-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74091-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74091-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74091-125">輸入</span><span class="sxs-lookup"><span data-stu-id="74091-125">INPUTS</span></span>

## <span data-ttu-id="74091-126">輸出</span><span class="sxs-lookup"><span data-stu-id="74091-126">OUTPUTS</span></span>

## <span data-ttu-id="74091-127">筆記</span><span class="sxs-lookup"><span data-stu-id="74091-127">NOTES</span></span>

## <span data-ttu-id="74091-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="74091-128">RELATED LINKS</span></span>

[<span data-ttu-id="74091-129">如何使用 Azure PowerShell for 媒體服務</span><span class="sxs-lookup"><span data-stu-id="74091-129">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)


