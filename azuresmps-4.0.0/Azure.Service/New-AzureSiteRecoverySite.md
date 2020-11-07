---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 43E5EC54-5DF4-4D32-8657-D7039DD04513
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68152b80711544a76abc17f697fe9730d1a6f1bc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967338"
---
# <span data-ttu-id="a9ee4-101">New-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="a9ee4-101">New-AzureSiteRecoverySite</span></span>

## <span data-ttu-id="a9ee4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ee4-103">建立網站恢復網站。</span><span class="sxs-lookup"><span data-stu-id="a9ee4-103">Creates a Site Recovery site.</span></span>

## <span data-ttu-id="a9ee4-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9ee4-104">SYNTAX</span></span>

```
New-AzureSiteRecoverySite -Name <String> [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a9ee4-105">說明</span><span class="sxs-lookup"><span data-stu-id="a9ee4-105">DESCRIPTION</span></span>
<span data-ttu-id="a9ee4-106">**新的 AzureSiteRecoverySite** Cmdlet 會在目前的電子倉庫中建立 Azure Site Recovery 網站。</span><span class="sxs-lookup"><span data-stu-id="a9ee4-106">The **New-AzureSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="a9ee4-107">示例</span><span class="sxs-lookup"><span data-stu-id="a9ee4-107">EXAMPLES</span></span>

### <span data-ttu-id="a9ee4-108">範例1：建立網站恢復網站</span><span class="sxs-lookup"><span data-stu-id="a9ee4-108">Example 1: Create a Site Recovery site</span></span>
```
PS C:\> New-AzureSiteRecoverySite -Name "RecoverySite07"
```

<span data-ttu-id="a9ee4-109">這個命令會建立名為 RecoverySite07 的網站復原網站。</span><span class="sxs-lookup"><span data-stu-id="a9ee4-109">This command creates a site recovery site named RecoverySite07.</span></span>

## <span data-ttu-id="a9ee4-110">參數</span><span class="sxs-lookup"><span data-stu-id="a9ee4-110">PARAMETERS</span></span>

### <span data-ttu-id="a9ee4-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="a9ee4-111">-Name</span></span>
<span data-ttu-id="a9ee4-112">指定網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9ee4-112">Specifies the name of the site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ee4-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a9ee4-113">-Profile</span></span>
<span data-ttu-id="a9ee4-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a9ee4-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a9ee4-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a9ee4-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a9ee4-116">-保存庫</span><span class="sxs-lookup"><span data-stu-id="a9ee4-116">-Vault</span></span>
<span data-ttu-id="a9ee4-117">指定要為其建立網站的保存庫。</span><span class="sxs-lookup"><span data-stu-id="a9ee4-117">Specifies a vault for which to create the site.</span></span>
<span data-ttu-id="a9ee4-118">若要取得 **ASRVault** 物件，請使用 **AzureSiteRecoveryVault** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9ee4-118">To obtain an **ASRVault** object, use the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>

```yaml
Type: ASRVault
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ee4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ee4-119">CommonParameters</span></span>
<span data-ttu-id="a9ee4-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9ee4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ee4-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a9ee4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ee4-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a9ee4-122">INPUTS</span></span>

## <span data-ttu-id="a9ee4-123">輸出</span><span class="sxs-lookup"><span data-stu-id="a9ee4-123">OUTPUTS</span></span>

## <span data-ttu-id="a9ee4-124">筆記</span><span class="sxs-lookup"><span data-stu-id="a9ee4-124">NOTES</span></span>

## <span data-ttu-id="a9ee4-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9ee4-125">RELATED LINKS</span></span>

[<span data-ttu-id="a9ee4-126">AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="a9ee4-126">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="a9ee4-127">AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="a9ee4-127">Get-AzureSiteRecoverySite</span></span>](./Get-AzureSiteRecoverySite.md)


