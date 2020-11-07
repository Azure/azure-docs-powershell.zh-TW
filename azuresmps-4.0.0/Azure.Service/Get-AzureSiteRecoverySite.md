---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6DD09F28-BFAE-4F9B-BF9C-F09767F9BFEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9151cb5a64b5873ab1c63420a97eb2e7bcffc0ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967023"
---
# <span data-ttu-id="28ffc-101">Get-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="28ffc-101">Get-AzureSiteRecoverySite</span></span>

## <span data-ttu-id="28ffc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="28ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="28ffc-103">從 Site Recovery 保存庫取得 Hyper-v 網站。</span><span class="sxs-lookup"><span data-stu-id="28ffc-103">Gets the Hyper-V sites from a Site Recovery vault.</span></span>

## <span data-ttu-id="28ffc-104">句法</span><span class="sxs-lookup"><span data-stu-id="28ffc-104">SYNTAX</span></span>

```
Get-AzureSiteRecoverySite [-Vault <ASRVault>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="28ffc-105">說明</span><span class="sxs-lookup"><span data-stu-id="28ffc-105">DESCRIPTION</span></span>
<span data-ttu-id="28ffc-106">**AzureSiteRecoverySite** Cmdlet 會取得 Azure Site Recovery 保存庫中的 hyper-v 網站。</span><span class="sxs-lookup"><span data-stu-id="28ffc-106">The **Get-AzureSiteRecoverySite** cmdlet gets the Hyper-V sites in an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="28ffc-107">示例</span><span class="sxs-lookup"><span data-stu-id="28ffc-107">EXAMPLES</span></span>

### <span data-ttu-id="28ffc-108">範例1：取得恢復網站</span><span class="sxs-lookup"><span data-stu-id="28ffc-108">Example 1: Get recovery sites</span></span>
```
PS C:\> Get-AzureSiteRecoverySite
Type                                    Name                                    ID
----                                    ----                                    --
HyperVSite                              RecoverySite07                          f16829b4-5b01-4209-a6cf-8e0aff1fe328
```

<span data-ttu-id="28ffc-109">這個命令會取得目前電子倉庫的恢復網站。</span><span class="sxs-lookup"><span data-stu-id="28ffc-109">This command gets the recovery sites for the current vault.</span></span>

## <span data-ttu-id="28ffc-110">參數</span><span class="sxs-lookup"><span data-stu-id="28ffc-110">PARAMETERS</span></span>

### <span data-ttu-id="28ffc-111">-設定檔</span><span class="sxs-lookup"><span data-stu-id="28ffc-111">-Profile</span></span>
<span data-ttu-id="28ffc-112">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="28ffc-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="28ffc-113">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="28ffc-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="28ffc-114">-保存庫</span><span class="sxs-lookup"><span data-stu-id="28ffc-114">-Vault</span></span>
<span data-ttu-id="28ffc-115">指定要取得網站的保存庫。</span><span class="sxs-lookup"><span data-stu-id="28ffc-115">Specifies a vault for which to get sites.</span></span>
<span data-ttu-id="28ffc-116">若要取得 **ASRVault** 物件，請使用 **AzureSiteRecoveryVault** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28ffc-116">To obtain an **ASRVault** object, use the **Get-AzureSiteRecoveryVault** cmdlet.</span></span>

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

### <span data-ttu-id="28ffc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28ffc-117">CommonParameters</span></span>
<span data-ttu-id="28ffc-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="28ffc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28ffc-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="28ffc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28ffc-120">輸入</span><span class="sxs-lookup"><span data-stu-id="28ffc-120">INPUTS</span></span>

## <span data-ttu-id="28ffc-121">輸出</span><span class="sxs-lookup"><span data-stu-id="28ffc-121">OUTPUTS</span></span>

## <span data-ttu-id="28ffc-122">筆記</span><span class="sxs-lookup"><span data-stu-id="28ffc-122">NOTES</span></span>

## <span data-ttu-id="28ffc-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="28ffc-123">RELATED LINKS</span></span>

[<span data-ttu-id="28ffc-124">AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="28ffc-124">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)

[<span data-ttu-id="28ffc-125">新-AzureSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="28ffc-125">New-AzureSiteRecoverySite</span></span>](./New-AzureSiteRecoverySite.md)


