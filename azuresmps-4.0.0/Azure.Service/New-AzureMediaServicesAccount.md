---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6C4081EE-0BCD-4285-8ABB-778BD95BFE4F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37f6e5b1152af79b2fc199199bf2b872bfbfa4ec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967357"
---
# <span data-ttu-id="7a8a6-101">New-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7a8a6-101">New-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="7a8a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7a8a6-102">SYNOPSIS</span></span>
<span data-ttu-id="7a8a6-103">建立 Azure 媒體服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="7a8a6-103">Creates an Azure Media Services account.</span></span>

<span data-ttu-id="7a8a6-104">**注意：** 此版本已棄用，請參閱 [較新的版本](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services)。</span><span class="sxs-lookup"><span data-stu-id="7a8a6-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="7a8a6-105">句法</span><span class="sxs-lookup"><span data-stu-id="7a8a6-105">SYNTAX</span></span>

```
New-AzureMediaServicesAccount -Name <String> -Location <String> -StorageAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7a8a6-106">說明</span><span class="sxs-lookup"><span data-stu-id="7a8a6-106">DESCRIPTION</span></span>
<span data-ttu-id="7a8a6-107">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7a8a6-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7a8a6-108">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="7a8a6-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7a8a6-109">**新的-AzureMediaServicesAccount** Cmdlet 會使用指定的媒體服務帳戶名稱、您要建立帳戶的 datacenter 位置，以及現有的儲存空間帳戶名稱，來建立新的媒體服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="7a8a6-109">The **New-AzureMediaServicesAccount** cmdlet creates a new Media Services account with the specified Media Services account name, datacenter location where you want to create the account, and an existing storage account name.</span></span>
<span data-ttu-id="7a8a6-110">儲存空間帳戶必須與新的媒體服務帳戶位於同一個資料中心。</span><span class="sxs-lookup"><span data-stu-id="7a8a6-110">The storage account has to be located in the same data center as the new Media Services account.</span></span>

## <span data-ttu-id="7a8a6-111">示例</span><span class="sxs-lookup"><span data-stu-id="7a8a6-111">EXAMPLES</span></span>

### <span data-ttu-id="7a8a6-112">範例1：建立新的媒體服務帳戶</span><span class="sxs-lookup"><span data-stu-id="7a8a6-112">Example 1: Create a new Media Services account</span></span>
```
PS C:\> New-AzureMediaServicesAccount -Name "mediaserviceaccount" -StorageAccountName "storageaccount " -Location "West US"
```

## <span data-ttu-id="7a8a6-113">參數</span><span class="sxs-lookup"><span data-stu-id="7a8a6-113">PARAMETERS</span></span>

### <span data-ttu-id="7a8a6-114">-位置</span><span class="sxs-lookup"><span data-stu-id="7a8a6-114">-Location</span></span>
<span data-ttu-id="7a8a6-115">指定媒體服務的 datacenter 位置。</span><span class="sxs-lookup"><span data-stu-id="7a8a6-115">Specifies the Media Services datacenter location.</span></span>

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

### <span data-ttu-id="7a8a6-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="7a8a6-116">-Name</span></span>
<span data-ttu-id="7a8a6-117">指定媒體服務帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="7a8a6-117">Specifies the Media Services account name.</span></span>

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

### <span data-ttu-id="7a8a6-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="7a8a6-118">-Profile</span></span>
<span data-ttu-id="7a8a6-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="7a8a6-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7a8a6-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="7a8a6-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7a8a6-121">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7a8a6-121">-StorageAccountName</span></span>
<span data-ttu-id="7a8a6-122">指定儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="7a8a6-122">Specifies the storage account name.</span></span>
<span data-ttu-id="7a8a6-123">儲存空間帳戶必須已經存在於與新媒體服務帳戶相同的資料中心中。</span><span class="sxs-lookup"><span data-stu-id="7a8a6-123">The storage account must already exist in the same datacenter as the new Media Services account.</span></span>

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

### <span data-ttu-id="7a8a6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a8a6-124">CommonParameters</span></span>
<span data-ttu-id="7a8a6-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7a8a6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a8a6-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7a8a6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a8a6-127">輸入</span><span class="sxs-lookup"><span data-stu-id="7a8a6-127">INPUTS</span></span>

## <span data-ttu-id="7a8a6-128">輸出</span><span class="sxs-lookup"><span data-stu-id="7a8a6-128">OUTPUTS</span></span>

## <span data-ttu-id="7a8a6-129">筆記</span><span class="sxs-lookup"><span data-stu-id="7a8a6-129">NOTES</span></span>

## <span data-ttu-id="7a8a6-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="7a8a6-130">RELATED LINKS</span></span>

[<span data-ttu-id="7a8a6-131">如何使用 Azure PowerShell for 媒體服務</span><span class="sxs-lookup"><span data-stu-id="7a8a6-131">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)

[<span data-ttu-id="7a8a6-132">AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7a8a6-132">Get-AzureMediaServicesAccount</span></span>](./Get-AzureMediaServicesAccount.md)

[<span data-ttu-id="7a8a6-133">移除-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7a8a6-133">Remove-AzureMediaServicesAccount</span></span>](./Remove-AzureMediaServicesAccount.md)


