---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D35C580F-437A-40F9-B6BA-412A1176292A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9821602df196604100de5926a7d9510bdb011bd2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967127"
---
# <span data-ttu-id="61178-101">Export-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="61178-101">Export-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="61178-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61178-102">SYNOPSIS</span></span>
<span data-ttu-id="61178-103">將一個 Azure RemoteApp 集合的範本影像匯出至指定的 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="61178-103">Exports the template image of one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="61178-104">句法</span><span class="sxs-lookup"><span data-stu-id="61178-104">SYNTAX</span></span>

```
Export-AzureRemoteAppTemplateImage [-CollectionName] <String> [-DestinationStorageAccountName] <String>
 [-DestinationStorageAccountKey] <String> [-DestinationStorageAccountContainerName] <String>
 [-OverwriteExistingTemplateImage] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61178-105">說明</span><span class="sxs-lookup"><span data-stu-id="61178-105">DESCRIPTION</span></span>
<span data-ttu-id="61178-106">**Export-AzureRemoteAppTemplateImage** Cmdlet 會將一個 Azure RemoteApp 集合的範本影像匯出至指定的 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="61178-106">The **Export-AzureRemoteAppTemplateImage** cmdlet exports the template image of one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="61178-107">示例</span><span class="sxs-lookup"><span data-stu-id="61178-107">EXAMPLES</span></span>

### <span data-ttu-id="61178-108">範例1：將範本影像匯出至 Azure 儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="61178-108">Example 1: Export a template image to the Azure storage account</span></span>
```
PS C:\> Export-AzureRemoteAppTemplateImage -CollectionName "Contoso" -DestinationStorageAccountName "AccountName" -DestinationStorageAccountKey "AccountKey" -DestinationStorageAccountContainerName "ContainerName" -OverwriteExistingTemplateImage
```

<span data-ttu-id="61178-109">這個命令會將名為 Contoso 的集合的範本圖像匯出為指定的 Azure 儲存空間帳戶中名為 [AccountName] 的容器，名稱是 [AccountName] 和 [金鑰 AccountKey]。</span><span class="sxs-lookup"><span data-stu-id="61178-109">This command exports the template image of the collection named Contoso to a container named ContainerName in the specified Azure storage account with name AccountName and key AccountKey.</span></span>

## <span data-ttu-id="61178-110">參數</span><span class="sxs-lookup"><span data-stu-id="61178-110">PARAMETERS</span></span>

### <span data-ttu-id="61178-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="61178-111">-CollectionName</span></span>
<span data-ttu-id="61178-112">指定來源 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="61178-112">Specifies the name of the source Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="61178-113">-DestinationStorageAccountContainerName</span><span class="sxs-lookup"><span data-stu-id="61178-113">-DestinationStorageAccountContainerName</span></span>
<span data-ttu-id="61178-114">指定目的地 Azure 儲存空間帳戶中之容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="61178-114">Specifies the name of a container in the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61178-115">-DestinationStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="61178-115">-DestinationStorageAccountKey</span></span>
<span data-ttu-id="61178-116">指定目的地 Azure 儲存空間帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="61178-116">Specifies the key of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61178-117">-DestinationStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="61178-117">-DestinationStorageAccountName</span></span>
<span data-ttu-id="61178-118">指定目的地 Azure 儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="61178-118">Specifies the name of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61178-119">-OverwriteExistingTemplateImage</span><span class="sxs-lookup"><span data-stu-id="61178-119">-OverwriteExistingTemplateImage</span></span>
<span data-ttu-id="61178-120">表示 Cmdlet 會覆寫現有的範本影像。</span><span class="sxs-lookup"><span data-stu-id="61178-120">Indicates that the cmdlet overwrites the existing template image.</span></span>

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

### <span data-ttu-id="61178-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="61178-121">-Profile</span></span>
<span data-ttu-id="61178-122">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="61178-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="61178-123">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="61178-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="61178-124">-確認</span><span class="sxs-lookup"><span data-stu-id="61178-124">-Confirm</span></span>
<span data-ttu-id="61178-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="61178-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61178-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61178-126">-WhatIf</span></span>
<span data-ttu-id="61178-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61178-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61178-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61178-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61178-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61178-129">CommonParameters</span></span>
<span data-ttu-id="61178-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61178-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61178-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="61178-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61178-132">輸入</span><span class="sxs-lookup"><span data-stu-id="61178-132">INPUTS</span></span>

## <span data-ttu-id="61178-133">輸出</span><span class="sxs-lookup"><span data-stu-id="61178-133">OUTPUTS</span></span>

## <span data-ttu-id="61178-134">筆記</span><span class="sxs-lookup"><span data-stu-id="61178-134">NOTES</span></span>

## <span data-ttu-id="61178-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="61178-135">RELATED LINKS</span></span>

[<span data-ttu-id="61178-136">AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="61178-136">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="61178-137">新-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="61178-137">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="61178-138">移除-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="61178-138">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="61178-139">重新命名 AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="61178-139">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


