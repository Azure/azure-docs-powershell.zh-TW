---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 3EC274C9-9BF6-4B39-BC70-C7F9D780805D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79b61501a56913fedb2a003d7aea1a041bfab4d5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412277"
---
# <span data-ttu-id="8c446-101">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="8c446-101">Get-AzureSiteRecoveryServer</span></span>

## <span data-ttu-id="8c446-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8c446-102">SYNOPSIS</span></span>
<span data-ttu-id="8c446-103">讓網站復原伺服器註冊網站復原儲存庫。</span><span class="sxs-lookup"><span data-stu-id="8c446-103">Gets Site Recovery servers registered a Site Recovery vault.</span></span>

## <span data-ttu-id="8c446-104">語法</span><span class="sxs-lookup"><span data-stu-id="8c446-104">SYNTAX</span></span>

### <span data-ttu-id="8c446-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="8c446-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryServer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8c446-106">ById</span><span class="sxs-lookup"><span data-stu-id="8c446-106">ById</span></span>
```
Get-AzureSiteRecoveryServer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8c446-107">ByName</span><span class="sxs-lookup"><span data-stu-id="8c446-107">ByName</span></span>
```
Get-AzureSiteRecoveryServer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8c446-108">描述</span><span class="sxs-lookup"><span data-stu-id="8c446-108">DESCRIPTION</span></span>
<span data-ttu-id="8c446-109">**Get-AzureSiteRecoveryServer** Cmdlet 會取得已註冊至目前網站復原保存庫的 Azure 網站復原伺服器相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8c446-109">The **Get-AzureSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="8c446-110">例子</span><span class="sxs-lookup"><span data-stu-id="8c446-110">EXAMPLES</span></span>

### <span data-ttu-id="8c446-111">範例 1：取得網站復原伺服器的資訊</span><span class="sxs-lookup"><span data-stu-id="8c446-111">Example 1: Get information about a Site Recovery server</span></span>
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

<span data-ttu-id="8c446-112">此命令會獲得有關 Azure 網站修復伺服器的資訊。</span><span class="sxs-lookup"><span data-stu-id="8c446-112">This command gets information about an Azure Site Recovery server.</span></span>

## <span data-ttu-id="8c446-113">參數</span><span class="sxs-lookup"><span data-stu-id="8c446-113">PARAMETERS</span></span>

### <span data-ttu-id="8c446-114">-Id</span><span class="sxs-lookup"><span data-stu-id="8c446-114">-Id</span></span>
<span data-ttu-id="8c446-115">指定伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c446-115">Specifies the ID of a server.</span></span>

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

### <span data-ttu-id="8c446-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c446-116">-Name</span></span>
<span data-ttu-id="8c446-117">指定伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c446-117">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="8c446-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8c446-118">-Profile</span></span>
<span data-ttu-id="8c446-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8c446-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8c446-120">如果您未指定設定檔，此 Cmdlet 會從本地預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8c446-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8c446-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c446-121">CommonParameters</span></span>
<span data-ttu-id="8c446-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8c446-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c446-123">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8c446-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c446-124">輸入</span><span class="sxs-lookup"><span data-stu-id="8c446-124">INPUTS</span></span>

## <span data-ttu-id="8c446-125">輸出</span><span class="sxs-lookup"><span data-stu-id="8c446-125">OUTPUTS</span></span>

## <span data-ttu-id="8c446-126">筆記</span><span class="sxs-lookup"><span data-stu-id="8c446-126">NOTES</span></span>

## <span data-ttu-id="8c446-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c446-127">RELATED LINKS</span></span>




