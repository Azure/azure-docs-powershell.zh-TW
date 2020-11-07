---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: A6B274EA-7FF2-46B0-8622-0DD17E9ADDD6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5531684de38a4a42aee4c131dbe58cd143370796
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93968023"
---
# <span data-ttu-id="493e2-101">Get-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="493e2-101">Get-AzureRemoteAppSession</span></span>

## <span data-ttu-id="493e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="493e2-102">SYNOPSIS</span></span>
<span data-ttu-id="493e2-103">列出集合的所有活動和中斷連接的 Azure RemoteApp 會話。</span><span class="sxs-lookup"><span data-stu-id="493e2-103">Lists all active and disconnected Azure RemoteApp sessions for a collection.</span></span>

## <span data-ttu-id="493e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="493e2-104">SYNTAX</span></span>

```
Get-AzureRemoteAppSession [-CollectionName] <String> [[-UserUpn] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="493e2-105">說明</span><span class="sxs-lookup"><span data-stu-id="493e2-105">DESCRIPTION</span></span>
<span data-ttu-id="493e2-106">**AzureRemoteAppSession** Cmdlet 會列出 azure remoteapp 集合的所有活動與中斷連線的 azure RemoteApp 會話。</span><span class="sxs-lookup"><span data-stu-id="493e2-106">The **Get-AzureRemoteAppSession** cmdlet lists all active and disconnected Azure RemoteApp sessions for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="493e2-107">示例</span><span class="sxs-lookup"><span data-stu-id="493e2-107">EXAMPLES</span></span>

### <span data-ttu-id="493e2-108">範例1：列出集合中的所有會話</span><span class="sxs-lookup"><span data-stu-id="493e2-108">Example 1: List all the sessions in a collection</span></span>
```
PS C:\> Get-AzureRemoteAppSession -CollectionName "ContosoApps"
```

<span data-ttu-id="493e2-109">這個命令會列出 Azure RemoteApp 集合中名為 ContosoApps 的所有會話。</span><span class="sxs-lookup"><span data-stu-id="493e2-109">This command lists all sessions in the Azure RemoteApp collection named ContosoApps.</span></span>

## <span data-ttu-id="493e2-110">參數</span><span class="sxs-lookup"><span data-stu-id="493e2-110">PARAMETERS</span></span>

### <span data-ttu-id="493e2-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="493e2-111">-CollectionName</span></span>
<span data-ttu-id="493e2-112">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="493e2-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="493e2-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="493e2-113">-Profile</span></span>
<span data-ttu-id="493e2-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="493e2-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="493e2-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="493e2-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="493e2-116">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="493e2-116">-UserUpn</span></span>
<span data-ttu-id="493e2-117">指定要取得 Azure RemoteApp 會話之使用者的使用者主要名稱 (UPN) 。</span><span class="sxs-lookup"><span data-stu-id="493e2-117">Specifies the user Principal Name (UPN) of a user for which to get Azure RemoteApp sessions.</span></span>
<span data-ttu-id="493e2-118">例如，UPN 可以是下列格式： PattiFuller@contoso.com 。</span><span class="sxs-lookup"><span data-stu-id="493e2-118">For example, the UPN can be in the following format: PattiFuller@contoso.com.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="493e2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="493e2-119">CommonParameters</span></span>
<span data-ttu-id="493e2-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="493e2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="493e2-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="493e2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="493e2-122">輸入</span><span class="sxs-lookup"><span data-stu-id="493e2-122">INPUTS</span></span>

## <span data-ttu-id="493e2-123">輸出</span><span class="sxs-lookup"><span data-stu-id="493e2-123">OUTPUTS</span></span>

## <span data-ttu-id="493e2-124">筆記</span><span class="sxs-lookup"><span data-stu-id="493e2-124">NOTES</span></span>

## <span data-ttu-id="493e2-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="493e2-125">RELATED LINKS</span></span>

[<span data-ttu-id="493e2-126">中斷連線-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="493e2-126">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="493e2-127">Invoke-AzureRemoteAppSessionLogoff</span><span class="sxs-lookup"><span data-stu-id="493e2-127">Invoke-AzureRemoteAppSessionLogoff</span></span>](./Invoke-AzureRemoteAppSessionLogoff.md)

[<span data-ttu-id="493e2-128">傳送 AzureRemoteAppSessionMessage</span><span class="sxs-lookup"><span data-stu-id="493e2-128">Send-AzureRemoteAppSessionMessage</span></span>](./Send-AzureRemoteAppSessionMessage.md)


