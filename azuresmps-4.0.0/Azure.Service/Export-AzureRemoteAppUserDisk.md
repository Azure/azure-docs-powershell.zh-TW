---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 72D332BA-A30B-45B9-875C-DF9D33299E05
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ddfbdc7da2f398ae1db11cf87de344c4f4ed5de
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967124"
---
# <span data-ttu-id="c943a-101">Export-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="c943a-101">Export-AzureRemoteAppUserDisk</span></span>

## <span data-ttu-id="c943a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c943a-102">SYNOPSIS</span></span>
<span data-ttu-id="c943a-103">將所有使用者磁片從一個 Azure RemoteApp 集合匯出到指定的 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c943a-103">Exports all user disks from one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="c943a-104">句法</span><span class="sxs-lookup"><span data-stu-id="c943a-104">SYNTAX</span></span>

```
Export-AzureRemoteAppUserDisk [-CollectionName] <String> [-DestinationStorageAccountName] <String>
 [-DestinationStorageAccountKey] <String> [-DestinationStorageAccountContainerName] <String>
 [-OverwriteExistingUserDisk] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c943a-105">說明</span><span class="sxs-lookup"><span data-stu-id="c943a-105">DESCRIPTION</span></span>
<span data-ttu-id="c943a-106">**Export-AzureRemoteAppUserDisk** Cmdlet 會將來自一個 azure RemoteApp 集合的所有使用者磁片匯出到指定的 Azure 儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="c943a-106">The **Export-AzureRemoteAppUserDisk** cmdlet exports all user disks from one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="c943a-107">示例</span><span class="sxs-lookup"><span data-stu-id="c943a-107">EXAMPLES</span></span>

### <span data-ttu-id="c943a-108">範例1：將集合中的所有使用者磁片匯出至指定的 Azure 儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="c943a-108">Example 1: Export all the user disks from a collection to the specified Azure storage account</span></span>
```
PS C:\> Export-AzureRemoteAppUserDisk -CollectionName "Contoso" -DestinationStorageAccountName "AccountName" -DestinationStorageAccountKey "AccountKey" -DestinationStorageAccountContainerName "ContainerName" -OverwriteExistingUserDisk
```

<span data-ttu-id="c943a-109">這個命令會將名為 Contoso 的集合中的所有使用者磁片匯出為指定之 Azure 儲存空間帳戶中名為 [AccountName] 的容器，名稱為 [AccountName] 和 [金鑰 AccountKey]。</span><span class="sxs-lookup"><span data-stu-id="c943a-109">This command exports all the user disks from the collection named Contoso to a container named ContainerName in the specified Azure storage account with name AccountName and key AccountKey.</span></span>

## <span data-ttu-id="c943a-110">參數</span><span class="sxs-lookup"><span data-stu-id="c943a-110">PARAMETERS</span></span>

### <span data-ttu-id="c943a-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="c943a-111">-CollectionName</span></span>
<span data-ttu-id="c943a-112">指定來源 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="c943a-112">Specifies the name of the source Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="c943a-113">-DestinationStorageAccountContainerName</span><span class="sxs-lookup"><span data-stu-id="c943a-113">-DestinationStorageAccountContainerName</span></span>
<span data-ttu-id="c943a-114">指定目的地 Azure 儲存空間帳戶中之容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c943a-114">Specifies the name of a container in the destination Azure storage account.</span></span>

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

### <span data-ttu-id="c943a-115">-DestinationStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c943a-115">-DestinationStorageAccountKey</span></span>
<span data-ttu-id="c943a-116">指定目的地 Azure 儲存空間帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="c943a-116">Specifies the Key of the destination Azure storage account.</span></span>

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

### <span data-ttu-id="c943a-117">-DestinationStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c943a-117">-DestinationStorageAccountName</span></span>
<span data-ttu-id="c943a-118">指定目的地 Azure 儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="c943a-118">Specifies the name of the destination Azure storage account.</span></span>

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

### <span data-ttu-id="c943a-119">-OverwriteExistingUserDisk</span><span class="sxs-lookup"><span data-stu-id="c943a-119">-OverwriteExistingUserDisk</span></span>
<span data-ttu-id="c943a-120">表示 Cmdlet 會覆寫現有的使用者磁片。</span><span class="sxs-lookup"><span data-stu-id="c943a-120">Indicates that the cmdlet overwrites the existing user disk.</span></span>

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

### <span data-ttu-id="c943a-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c943a-121">-Profile</span></span>
<span data-ttu-id="c943a-122">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c943a-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c943a-123">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c943a-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c943a-124">-確認</span><span class="sxs-lookup"><span data-stu-id="c943a-124">-Confirm</span></span>
<span data-ttu-id="c943a-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c943a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c943a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c943a-126">-WhatIf</span></span>
<span data-ttu-id="c943a-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c943a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c943a-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c943a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c943a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c943a-129">CommonParameters</span></span>
<span data-ttu-id="c943a-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c943a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c943a-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c943a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c943a-132">輸入</span><span class="sxs-lookup"><span data-stu-id="c943a-132">INPUTS</span></span>

## <span data-ttu-id="c943a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="c943a-133">OUTPUTS</span></span>

## <span data-ttu-id="c943a-134">筆記</span><span class="sxs-lookup"><span data-stu-id="c943a-134">NOTES</span></span>

## <span data-ttu-id="c943a-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="c943a-135">RELATED LINKS</span></span>

[<span data-ttu-id="c943a-136">複製 AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="c943a-136">Copy-AzureRemoteAppUserDisk</span></span>](./Copy-AzureRemoteAppUserDisk.md)

[<span data-ttu-id="c943a-137">移除-AzureRemoteAppUserDisk</span><span class="sxs-lookup"><span data-stu-id="c943a-137">Remove-AzureRemoteAppUserDisk</span></span>](./Remove-AzureRemoteAppUserDisk.md)


