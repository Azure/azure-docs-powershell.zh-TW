---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 22571840-C27C-4208-A755-EF89E6C4B604
online version: ''
schema: 2.0.0
ms.openlocfilehash: 61cfeab9e02968c7b03e694b9913d4cbe4b3c90a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966920"
---
# <span data-ttu-id="362c5-101">Rename-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="362c5-101">Rename-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="362c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="362c5-102">SYNOPSIS</span></span>
<span data-ttu-id="362c5-103">重新命名 Azure RemoteApp 範本影像。</span><span class="sxs-lookup"><span data-stu-id="362c5-103">Renames an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="362c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="362c5-104">SYNTAX</span></span>

```
Rename-AzureRemoteAppTemplateImage [-ImageName] <String> [-NewName] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="362c5-105">說明</span><span class="sxs-lookup"><span data-stu-id="362c5-105">DESCRIPTION</span></span>
<span data-ttu-id="362c5-106">**Rename AzureRemoteAppTemplateImage** Cmdlet 會重新命名 Azure RemoteApp 範本影像。</span><span class="sxs-lookup"><span data-stu-id="362c5-106">The **Rename-AzureRemoteAppTemplateImage** cmdlet renames an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="362c5-107">示例</span><span class="sxs-lookup"><span data-stu-id="362c5-107">EXAMPLES</span></span>

### <span data-ttu-id="362c5-108">範例1：重新命名範本圖像</span><span class="sxs-lookup"><span data-stu-id="362c5-108">Example 1: Rename a template image</span></span>
```
PS C:\> Rename-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -NewName "ContosoFinanceApps"
```

<span data-ttu-id="362c5-109">這個命令會將名為 ContosoApps 的 Azure RemoteApp 範本影像重新命名為 ContosoFinanceApps。</span><span class="sxs-lookup"><span data-stu-id="362c5-109">This command renames the Azure RemoteApp template image named ContosoApps to ContosoFinanceApps.</span></span>

## <span data-ttu-id="362c5-110">參數</span><span class="sxs-lookup"><span data-stu-id="362c5-110">PARAMETERS</span></span>

### <span data-ttu-id="362c5-111">-ImageName</span><span class="sxs-lookup"><span data-stu-id="362c5-111">-ImageName</span></span>
<span data-ttu-id="362c5-112">指定要重新命名之 Azure RemoteApp 範本映射的名稱。</span><span class="sxs-lookup"><span data-stu-id="362c5-112">Specifies the name of an Azure RemoteApp template image to rename.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="362c5-113">-NewName</span><span class="sxs-lookup"><span data-stu-id="362c5-113">-NewName</span></span>
<span data-ttu-id="362c5-114">指定 Azure RemoteApp 範本影像的新名稱。</span><span class="sxs-lookup"><span data-stu-id="362c5-114">Specifies a new name for an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="362c5-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="362c5-115">-Profile</span></span>
<span data-ttu-id="362c5-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="362c5-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="362c5-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="362c5-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="362c5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="362c5-118">CommonParameters</span></span>
<span data-ttu-id="362c5-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="362c5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="362c5-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="362c5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="362c5-121">輸入</span><span class="sxs-lookup"><span data-stu-id="362c5-121">INPUTS</span></span>

## <span data-ttu-id="362c5-122">輸出</span><span class="sxs-lookup"><span data-stu-id="362c5-122">OUTPUTS</span></span>

## <span data-ttu-id="362c5-123">筆記</span><span class="sxs-lookup"><span data-stu-id="362c5-123">NOTES</span></span>

## <span data-ttu-id="362c5-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="362c5-124">RELATED LINKS</span></span>

[<span data-ttu-id="362c5-125">AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="362c5-125">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="362c5-126">新-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="362c5-126">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="362c5-127">移除-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="362c5-127">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)


