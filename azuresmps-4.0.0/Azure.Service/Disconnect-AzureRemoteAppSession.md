---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 514C33F8-F0B8-4F37-AB2D-BB54DD754931
online version: ''
schema: 2.0.0
ms.openlocfilehash: c256ce8ba720eb08ffec2ab56ecca40ab74f4948
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967132"
---
# <span data-ttu-id="3ecb6-101">Disconnect-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="3ecb6-101">Disconnect-AzureRemoteAppSession</span></span>

## <span data-ttu-id="3ecb6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ecb6-102">SYNOPSIS</span></span>
<span data-ttu-id="3ecb6-103">中斷 Azure RemoteApp 會話的連線。</span><span class="sxs-lookup"><span data-stu-id="3ecb6-103">Disconnects an Azure RemoteApp session.</span></span>

## <span data-ttu-id="3ecb6-104">句法</span><span class="sxs-lookup"><span data-stu-id="3ecb6-104">SYNTAX</span></span>

```
Disconnect-AzureRemoteAppSession [-CollectionName] <String> [-UserUpn] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ecb6-105">說明</span><span class="sxs-lookup"><span data-stu-id="3ecb6-105">DESCRIPTION</span></span>
<span data-ttu-id="3ecb6-106">**Disconnect AzureRemoteAppSession** Cmdlet 會中斷使用者的 Azure RemoteApp 會話連線。</span><span class="sxs-lookup"><span data-stu-id="3ecb6-106">The **Disconnect-AzureRemoteAppSession** cmdlet disconnects a user's Azure RemoteApp session.</span></span>
<span data-ttu-id="3ecb6-107">使用者的用戶端從其 Azure RemoteApp 會話斷開連線，但使用者的程式仍會繼續執行。</span><span class="sxs-lookup"><span data-stu-id="3ecb6-107">The user's client disconnects from their Azure RemoteApp session, but the user's programs continue to run.</span></span>

## <span data-ttu-id="3ecb6-108">示例</span><span class="sxs-lookup"><span data-stu-id="3ecb6-108">EXAMPLES</span></span>

### <span data-ttu-id="3ecb6-109">範例1：中斷使用者會話的連線</span><span class="sxs-lookup"><span data-stu-id="3ecb6-109">Example 1: Disconnect a user's session</span></span>
```
PS C:\> Disconnect-AzureRemoteAppSession -CollectionName "ContosoApps" -UserUpn "PattiFuller@contoso.com"
```

<span data-ttu-id="3ecb6-110">這個命令會中斷 ContosoApps 集合中的 Azure RemoteApp 會話與 UPN 的使用者之間的連線 PattiFuller@contoso.com 。</span><span class="sxs-lookup"><span data-stu-id="3ecb6-110">This command disconnects the Azure RemoteApp session in the ContosoApps collection for the user whose UPN is PattiFuller@contoso.com.</span></span>

## <span data-ttu-id="3ecb6-111">參數</span><span class="sxs-lookup"><span data-stu-id="3ecb6-111">PARAMETERS</span></span>

### <span data-ttu-id="3ecb6-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="3ecb6-112">-CollectionName</span></span>
<span data-ttu-id="3ecb6-113">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ecb6-113">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="3ecb6-114">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3ecb6-114">-Profile</span></span>
<span data-ttu-id="3ecb6-115">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3ecb6-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3ecb6-116">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="3ecb6-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3ecb6-117">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="3ecb6-117">-UserUpn</span></span>
<span data-ttu-id="3ecb6-118">指定使用者的使用者主要名稱 (UPN) PattiFuller@contoso.com 。</span><span class="sxs-lookup"><span data-stu-id="3ecb6-118">Specifies the User Principal Name (UPN) of a user, for example PattiFuller@contoso.com.</span></span>

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

### <span data-ttu-id="3ecb6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ecb6-119">CommonParameters</span></span>
<span data-ttu-id="3ecb6-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ecb6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ecb6-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3ecb6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ecb6-122">輸入</span><span class="sxs-lookup"><span data-stu-id="3ecb6-122">INPUTS</span></span>

## <span data-ttu-id="3ecb6-123">輸出</span><span class="sxs-lookup"><span data-stu-id="3ecb6-123">OUTPUTS</span></span>

## <span data-ttu-id="3ecb6-124">筆記</span><span class="sxs-lookup"><span data-stu-id="3ecb6-124">NOTES</span></span>

## <span data-ttu-id="3ecb6-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ecb6-125">RELATED LINKS</span></span>

[<span data-ttu-id="3ecb6-126">AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="3ecb6-126">Get-AzureRemoteAppSession</span></span>](./Get-AzureRemoteAppSession.md)

[<span data-ttu-id="3ecb6-127">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="3ecb6-127">Invoke-AzureRemoteAppSessionLogoff</span></span>](./Invoke-AzureRemoteAppSessionLogoff.md)

[<span data-ttu-id="3ecb6-128">傳送 AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="3ecb6-128">Send-AzureRemoteAppSessionMessage</span></span>](./Send-AzureRemoteAppSessionMessage.md)


