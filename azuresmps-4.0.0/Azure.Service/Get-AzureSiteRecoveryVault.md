---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2A6DDF5F-2906-4DB5-B791-B6BF590261A0
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffdf63e9e4d1d8e34dc63cb90c1fa0de15369fbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93968011"
---
# <span data-ttu-id="a2ace-101">Get-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="a2ace-101">Get-AzureSiteRecoveryVault</span></span>

## <span data-ttu-id="a2ace-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2ace-102">SYNOPSIS</span></span>
<span data-ttu-id="a2ace-103">從目前的訂閱取得網站復原保存庫。</span><span class="sxs-lookup"><span data-stu-id="a2ace-103">Gets Site Recovery vaults from the current subscription.</span></span>

## <span data-ttu-id="a2ace-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2ace-104">SYNTAX</span></span>

### <span data-ttu-id="a2ace-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="a2ace-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryVault [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a2ace-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a2ace-106">ByName</span></span>
```
Get-AzureSiteRecoveryVault -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a2ace-107">說明</span><span class="sxs-lookup"><span data-stu-id="a2ace-107">DESCRIPTION</span></span>
<span data-ttu-id="a2ace-108">**AzureSiteRecoveryVault** Cmdlet 會從目前的訂閱取得 Azure Site recovery 保存庫或特定網站復原保存庫的清單。</span><span class="sxs-lookup"><span data-stu-id="a2ace-108">The **Get-AzureSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="a2ace-109">示例</span><span class="sxs-lookup"><span data-stu-id="a2ace-109">EXAMPLES</span></span>

### <span data-ttu-id="a2ace-110">範例1：取得作用中的電子倉庫</span><span class="sxs-lookup"><span data-stu-id="a2ace-110">Example 1: Get the active vault</span></span>
```
PS C:\> Get-AzureSiteRecoveryVault
Name             : ContosoVault
ID               : 6467459117394545458
CloudServiceName : CS-West-US-RecoveryServices
SubscriptionId   : a5aa5997-33e5-46cc-8ab8-b8d89b76b7ba
StatusReason     : 
Status           : Active
Location         : West US
```

<span data-ttu-id="a2ace-111">這個命令會取得 active Azure Site Recovery 保存庫。</span><span class="sxs-lookup"><span data-stu-id="a2ace-111">This command gets the active Azure Site Recovery vault.</span></span>

## <span data-ttu-id="a2ace-112">參數</span><span class="sxs-lookup"><span data-stu-id="a2ace-112">PARAMETERS</span></span>

### <span data-ttu-id="a2ace-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2ace-113">-Name</span></span>
<span data-ttu-id="a2ace-114">指定要取得之保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2ace-114">Specifies the name of the vault to get.</span></span>

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

### <span data-ttu-id="a2ace-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a2ace-115">-Profile</span></span>
<span data-ttu-id="a2ace-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a2ace-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a2ace-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a2ace-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a2ace-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2ace-118">CommonParameters</span></span>
<span data-ttu-id="a2ace-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2ace-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2ace-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a2ace-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2ace-121">輸入</span><span class="sxs-lookup"><span data-stu-id="a2ace-121">INPUTS</span></span>

## <span data-ttu-id="a2ace-122">輸出</span><span class="sxs-lookup"><span data-stu-id="a2ace-122">OUTPUTS</span></span>

## <span data-ttu-id="a2ace-123">筆記</span><span class="sxs-lookup"><span data-stu-id="a2ace-123">NOTES</span></span>

## <span data-ttu-id="a2ace-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2ace-124">RELATED LINKS</span></span>

[<span data-ttu-id="a2ace-125">新-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="a2ace-125">New-AzureSiteRecoveryVault</span></span>](./New-AzureSiteRecoveryVault.md)


