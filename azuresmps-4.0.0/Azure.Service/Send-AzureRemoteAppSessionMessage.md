---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 6236AD2C-D54D-4013-9977-AD1E6EAC2F21
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac0283f6c9de9a1cd5f17abd6e27ebb2c8629505
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967879"
---
# <span data-ttu-id="86cb1-101">Send-AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="86cb1-101">Send-AzureRemoteAppSessionMessage</span></span>

## <span data-ttu-id="86cb1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="86cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="86cb1-103">將訊息傳送給使用者。</span><span class="sxs-lookup"><span data-stu-id="86cb1-103">Sends a message to a user.</span></span>

## <span data-ttu-id="86cb1-104">句法</span><span class="sxs-lookup"><span data-stu-id="86cb1-104">SYNTAX</span></span>

```
Send-AzureRemoteAppSessionMessage [-CollectionName] <String> [-UserUpn] <String> [-Message] <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="86cb1-105">說明</span><span class="sxs-lookup"><span data-stu-id="86cb1-105">DESCRIPTION</span></span>
<span data-ttu-id="86cb1-106">AzureRemoteAppSessionMessage Cmdlet 會將訊息 **傳送** 給連線至 Azure RemoteApp 會話的使用者。</span><span class="sxs-lookup"><span data-stu-id="86cb1-106">The **Send-AzureRemoteAppSessionMessage** cmdlet sends a message to a user who is connected to an Azure RemoteApp session.</span></span>

## <span data-ttu-id="86cb1-107">示例</span><span class="sxs-lookup"><span data-stu-id="86cb1-107">EXAMPLES</span></span>

### <span data-ttu-id="86cb1-108">範例1：傳送訊息給使用者</span><span class="sxs-lookup"><span data-stu-id="86cb1-108">Example 1: Send a message to a user</span></span>
```
PS C:\> Send-AzureRemoteAppSessionMessage -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com" -Message "The system will be going down for maintenance soon.  Please save your work and close your RemoteApps."
```

<span data-ttu-id="86cb1-109">這個命令會將訊息傳送給其 UPN 的使用者 PattiFuller@contoso.com 。</span><span class="sxs-lookup"><span data-stu-id="86cb1-109">This command sends a message to the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="86cb1-110">參數</span><span class="sxs-lookup"><span data-stu-id="86cb1-110">PARAMETERS</span></span>

### <span data-ttu-id="86cb1-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="86cb1-111">-CollectionName</span></span>
<span data-ttu-id="86cb1-112">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="86cb1-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="86cb1-113">-訊息</span><span class="sxs-lookup"><span data-stu-id="86cb1-113">-Message</span></span>
<span data-ttu-id="86cb1-114">指定要傳送的訊息。</span><span class="sxs-lookup"><span data-stu-id="86cb1-114">Specifies the message to send.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86cb1-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="86cb1-115">-Profile</span></span>
<span data-ttu-id="86cb1-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="86cb1-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="86cb1-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="86cb1-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="86cb1-118">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="86cb1-118">-UserUpn</span></span>
<span data-ttu-id="86cb1-119">指定使用者的使用者主要名稱 (UPN) ，例如 PattiFuller@contoso.com 。</span><span class="sxs-lookup"><span data-stu-id="86cb1-119">Specifies the User Principal Name (UPN) of a user, for example, PattiFuller@contoso.com.</span></span>

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

### <span data-ttu-id="86cb1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86cb1-120">CommonParameters</span></span>
<span data-ttu-id="86cb1-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="86cb1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86cb1-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="86cb1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86cb1-123">輸入</span><span class="sxs-lookup"><span data-stu-id="86cb1-123">INPUTS</span></span>

## <span data-ttu-id="86cb1-124">輸出</span><span class="sxs-lookup"><span data-stu-id="86cb1-124">OUTPUTS</span></span>

## <span data-ttu-id="86cb1-125">筆記</span><span class="sxs-lookup"><span data-stu-id="86cb1-125">NOTES</span></span>

## <span data-ttu-id="86cb1-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="86cb1-126">RELATED LINKS</span></span>

[<span data-ttu-id="86cb1-127">附加 AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="86cb1-127">Add-AzureRemoteAppUser</span></span>](./Add-AzureRemoteAppUser.md)

[<span data-ttu-id="86cb1-128">AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="86cb1-128">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="86cb1-129">AzureRemoteAppUser</span><span class="sxs-lookup"><span data-stu-id="86cb1-129">Get-AzureRemoteAppUser</span></span>](./Get-AzureRemoteAppUser.md)


