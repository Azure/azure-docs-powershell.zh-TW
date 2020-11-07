---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 67890A2A-7922-4E4A-96B4-B58CF532D2DE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75a949128309e2777984be0dac33f27b0bc53aab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967183"
---
# <span data-ttu-id="5ab8b-101">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="5ab8b-101">Update-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="5ab8b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ab8b-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab8b-103">使用新的範本影像更新 Azure RemoteApp 集合。</span><span class="sxs-lookup"><span data-stu-id="5ab8b-103">Updates an Azure RemoteApp collection with a new template image.</span></span>

## <span data-ttu-id="5ab8b-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ab8b-104">SYNTAX</span></span>

```
Update-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [[-SubnetName] <String>]
 [-ForceLogoffWhenUpdateComplete] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ab8b-105">說明</span><span class="sxs-lookup"><span data-stu-id="5ab8b-105">DESCRIPTION</span></span>
<span data-ttu-id="5ab8b-106">**AzureRemoteAppCollection** Cmdlet 會使用新的範本影像來更新 Azure RemoteApp 集合。</span><span class="sxs-lookup"><span data-stu-id="5ab8b-106">The **Update-AzureRemoteAppCollection** cmdlet updates an Azure RemoteApp collection with a new template image.</span></span>
<span data-ttu-id="5ab8b-107">更新完成後，擁有現有會話的使用者在被自動登出前，會有一小時的時間登出。當他們再次登入時，會連線到新更新的集合。</span><span class="sxs-lookup"><span data-stu-id="5ab8b-107">After the update completes, users with existing sessions have one hour to sign out before they are automatically signed out. When they sign in again, they connect to the newly updated collection.</span></span>
<span data-ttu-id="5ab8b-108">若要強制在集合更新後立即登出使用者，請指定 *ForceLogoffWhenUpdateComplete* 參數。</span><span class="sxs-lookup"><span data-stu-id="5ab8b-108">To force users to be immediately signed out as soon as the collection is updated, specify the *ForceLogoffWhenUpdateComplete* parameter.</span></span>

## <span data-ttu-id="5ab8b-109">示例</span><span class="sxs-lookup"><span data-stu-id="5ab8b-109">EXAMPLES</span></span>

## <span data-ttu-id="5ab8b-110">參數</span><span class="sxs-lookup"><span data-stu-id="5ab8b-110">PARAMETERS</span></span>

### <span data-ttu-id="5ab8b-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="5ab8b-111">-CollectionName</span></span>
<span data-ttu-id="5ab8b-112">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ab8b-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ab8b-113">-ForceLogoffWhenUpdateComplete</span><span class="sxs-lookup"><span data-stu-id="5ab8b-113">-ForceLogoffWhenUpdateComplete</span></span>
<span data-ttu-id="5ab8b-114">表示此 Cmdlet 在更新完成後立即從現有的會話中登入。</span><span class="sxs-lookup"><span data-stu-id="5ab8b-114">Indicates that this cmdlet signs users out of their existing sessions as soon as the update is complete.</span></span>
<span data-ttu-id="5ab8b-115">當使用者再次登入時，他們會連線至新近更新的集合。</span><span class="sxs-lookup"><span data-stu-id="5ab8b-115">When users sign in again, they connect to the newly updated collection.</span></span>

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

### <span data-ttu-id="5ab8b-116">-ImageName</span><span class="sxs-lookup"><span data-stu-id="5ab8b-116">-ImageName</span></span>
<span data-ttu-id="5ab8b-117">指定 Azure RemoteApp 範本影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ab8b-117">Specifies the name of an Azure RemoteApp template image.</span></span>

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

### <span data-ttu-id="5ab8b-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5ab8b-118">-Profile</span></span>
<span data-ttu-id="5ab8b-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5ab8b-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5ab8b-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="5ab8b-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5ab8b-121">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="5ab8b-121">-SubnetName</span></span>
<span data-ttu-id="5ab8b-122">指定要將集合移動到哪個子網上的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ab8b-122">Specifies the name of the subnet into which to move the collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ab8b-123">-確認</span><span class="sxs-lookup"><span data-stu-id="5ab8b-123">-Confirm</span></span>
<span data-ttu-id="5ab8b-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5ab8b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ab8b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ab8b-125">-WhatIf</span></span>
<span data-ttu-id="5ab8b-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5ab8b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ab8b-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ab8b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ab8b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab8b-128">CommonParameters</span></span>
<span data-ttu-id="5ab8b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ab8b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab8b-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ab8b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab8b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="5ab8b-131">INPUTS</span></span>

## <span data-ttu-id="5ab8b-132">輸出</span><span class="sxs-lookup"><span data-stu-id="5ab8b-132">OUTPUTS</span></span>

## <span data-ttu-id="5ab8b-133">筆記</span><span class="sxs-lookup"><span data-stu-id="5ab8b-133">NOTES</span></span>

## <span data-ttu-id="5ab8b-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ab8b-134">RELATED LINKS</span></span>

[<span data-ttu-id="5ab8b-135">AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="5ab8b-135">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="5ab8b-136">新-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="5ab8b-136">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="5ab8b-137">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="5ab8b-137">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)


