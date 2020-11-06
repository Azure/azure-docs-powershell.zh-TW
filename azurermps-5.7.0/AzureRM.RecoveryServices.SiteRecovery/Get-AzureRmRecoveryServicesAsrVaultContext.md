---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 2be1ca7de1728d1aed7758cd170cb608c7645f18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454159"
---
# <span data-ttu-id="b77a7-101">Get-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="b77a7-101">Get-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="b77a7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b77a7-102">SYNOPSIS</span></span>
<span data-ttu-id="b77a7-103">取得恢復服務電子倉庫的 ASR vault 設定資訊。</span><span class="sxs-lookup"><span data-stu-id="b77a7-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b77a7-104">句法</span><span class="sxs-lookup"><span data-stu-id="b77a7-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b77a7-105">說明</span><span class="sxs-lookup"><span data-stu-id="b77a7-105">DESCRIPTION</span></span>
<span data-ttu-id="b77a7-106">**AzureRmRecoveryServicesAsrVaultCoNtext** Cmdlet 會取得與 [恢復服務] 保存庫相關的 ASR vault 設定資訊。</span><span class="sxs-lookup"><span data-stu-id="b77a7-106">The **Get-AzureRmRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="b77a7-107">示例</span><span class="sxs-lookup"><span data-stu-id="b77a7-107">EXAMPLES</span></span>

### <span data-ttu-id="b77a7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b77a7-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzureRmRecoveryServicesAsrVaultContext
```

<span data-ttu-id="b77a7-109">取得 PowerShell 會話) 復原服務電子倉庫中目前作用中 (的 ASR vault 設定。</span><span class="sxs-lookup"><span data-stu-id="b77a7-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="b77a7-110">參數</span><span class="sxs-lookup"><span data-stu-id="b77a7-110">PARAMETERS</span></span>

### <span data-ttu-id="b77a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b77a7-111">-DefaultProfile</span></span>
<span data-ttu-id="b77a7-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b77a7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77a7-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b77a7-113">CommonParameters</span></span>
<span data-ttu-id="b77a7-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b77a7-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b77a7-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b77a7-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b77a7-116">輸入</span><span class="sxs-lookup"><span data-stu-id="b77a7-116">INPUTS</span></span>

### <span data-ttu-id="b77a7-117">所有</span><span class="sxs-lookup"><span data-stu-id="b77a7-117">None</span></span>

## <span data-ttu-id="b77a7-118">輸出</span><span class="sxs-lookup"><span data-stu-id="b77a7-118">OUTPUTS</span></span>

### <span data-ttu-id="b77a7-119">RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="b77a7-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="b77a7-120">筆記</span><span class="sxs-lookup"><span data-stu-id="b77a7-120">NOTES</span></span>

## <span data-ttu-id="b77a7-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="b77a7-121">RELATED LINKS</span></span>