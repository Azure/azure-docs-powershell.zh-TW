---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 3EC274C9-9BF6-4B39-BC70-C7F9D780805D
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4081d6d072aadd6a4ae7d09ff57748a8f2cb697
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967026"
---
# <span data-ttu-id="65f23-101">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="65f23-101">Get-AzureSiteRecoveryServer</span></span>

## <span data-ttu-id="65f23-102">摘要</span><span class="sxs-lookup"><span data-stu-id="65f23-102">SYNOPSIS</span></span>
<span data-ttu-id="65f23-103">取得網站復原伺服器已登錄網站復原電子倉庫的註冊。</span><span class="sxs-lookup"><span data-stu-id="65f23-103">Gets Site Recovery servers registered a Site Recovery vault.</span></span>

## <span data-ttu-id="65f23-104">句法</span><span class="sxs-lookup"><span data-stu-id="65f23-104">SYNTAX</span></span>

### <span data-ttu-id="65f23-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="65f23-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryServer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="65f23-106">ById</span><span class="sxs-lookup"><span data-stu-id="65f23-106">ById</span></span>
```
Get-AzureSiteRecoveryServer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="65f23-107">ByName</span><span class="sxs-lookup"><span data-stu-id="65f23-107">ByName</span></span>
```
Get-AzureSiteRecoveryServer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="65f23-108">說明</span><span class="sxs-lookup"><span data-stu-id="65f23-108">DESCRIPTION</span></span>
<span data-ttu-id="65f23-109">**AzureSiteRecoveryServer** Cmdlet 會取得已登錄至目前網站復原電子倉庫之 Azure 網站復原伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="65f23-109">The **Get-AzureSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="65f23-110">示例</span><span class="sxs-lookup"><span data-stu-id="65f23-110">EXAMPLES</span></span>

### <span data-ttu-id="65f23-111">範例1：取得有關網站恢復伺服器的資訊</span><span class="sxs-lookup"><span data-stu-id="65f23-111">Example 1: Get information about a Site Recovery server</span></span>
```
PS C:\> Get-AzureSiteRecoveryServer
ID              : cd7dec80-1144-4531-9ab3-888b8ab39bee
Name            : server1.contoso.com
LastHeartbeat   : 9/23/2014 3:51:22 PM
ProviderVersion : 3.5.520.0
ServerVersion   : 3.2.7634.0

ID              : f5e713fe-5b6d-4641-9690-6fe74c976b8e
Name            : Server2.contoso.com
LastHeartbeat   : 8/13/2014 2:28:58 PM
ProviderVersion : 3.5
ServerVersion   : 3.2.7510.0
```

<span data-ttu-id="65f23-112">這個命令會取得 Azure Site Recovery 伺服器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="65f23-112">This command gets information about an Azure Site Recovery server.</span></span>

## <span data-ttu-id="65f23-113">參數</span><span class="sxs-lookup"><span data-stu-id="65f23-113">PARAMETERS</span></span>

### <span data-ttu-id="65f23-114">-識別碼</span><span class="sxs-lookup"><span data-stu-id="65f23-114">-Id</span></span>
<span data-ttu-id="65f23-115">指定伺服器的 ID。</span><span class="sxs-lookup"><span data-stu-id="65f23-115">Specifies the ID of a server.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65f23-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="65f23-116">-Name</span></span>
<span data-ttu-id="65f23-117">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="65f23-117">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65f23-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="65f23-118">-Profile</span></span>
<span data-ttu-id="65f23-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="65f23-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="65f23-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="65f23-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="65f23-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65f23-121">CommonParameters</span></span>
<span data-ttu-id="65f23-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="65f23-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65f23-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="65f23-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65f23-124">輸入</span><span class="sxs-lookup"><span data-stu-id="65f23-124">INPUTS</span></span>

## <span data-ttu-id="65f23-125">輸出</span><span class="sxs-lookup"><span data-stu-id="65f23-125">OUTPUTS</span></span>

## <span data-ttu-id="65f23-126">筆記</span><span class="sxs-lookup"><span data-stu-id="65f23-126">NOTES</span></span>

## <span data-ttu-id="65f23-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="65f23-127">RELATED LINKS</span></span>

[<span data-ttu-id="65f23-128">Azure Site Recovery 服務 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="65f23-128">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


