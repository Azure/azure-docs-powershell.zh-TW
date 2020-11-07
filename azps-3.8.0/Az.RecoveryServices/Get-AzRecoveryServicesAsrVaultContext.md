---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: cc8f5028a5b2d4917e94ebc666c478ee8d04efa7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956841"
---
# <span data-ttu-id="0c9bc-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="0c9bc-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="0c9bc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0c9bc-102">SYNOPSIS</span></span>
<span data-ttu-id="0c9bc-103">取得恢復服務電子倉庫的 ASR vault 設定資訊。</span><span class="sxs-lookup"><span data-stu-id="0c9bc-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="0c9bc-104">句法</span><span class="sxs-lookup"><span data-stu-id="0c9bc-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c9bc-105">說明</span><span class="sxs-lookup"><span data-stu-id="0c9bc-105">DESCRIPTION</span></span>
<span data-ttu-id="0c9bc-106">**AzRecoveryServicesAsrVaultCoNtext** Cmdlet 會取得與 [恢復服務] 保存庫相關的 ASR vault 設定資訊。</span><span class="sxs-lookup"><span data-stu-id="0c9bc-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="0c9bc-107">示例</span><span class="sxs-lookup"><span data-stu-id="0c9bc-107">EXAMPLES</span></span>

### <span data-ttu-id="0c9bc-108">範例1</span><span class="sxs-lookup"><span data-stu-id="0c9bc-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="0c9bc-109">取得 PowerShell 會話) 復原服務電子倉庫中目前作用中 (的 ASR vault 設定。</span><span class="sxs-lookup"><span data-stu-id="0c9bc-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="0c9bc-110">參數</span><span class="sxs-lookup"><span data-stu-id="0c9bc-110">PARAMETERS</span></span>

### <span data-ttu-id="0c9bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c9bc-111">-DefaultProfile</span></span>
<span data-ttu-id="0c9bc-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c9bc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c9bc-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c9bc-113">CommonParameters</span></span>
<span data-ttu-id="0c9bc-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0c9bc-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c9bc-115">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0c9bc-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c9bc-116">輸入</span><span class="sxs-lookup"><span data-stu-id="0c9bc-116">INPUTS</span></span>

### <span data-ttu-id="0c9bc-117">所有</span><span class="sxs-lookup"><span data-stu-id="0c9bc-117">None</span></span>

## <span data-ttu-id="0c9bc-118">輸出</span><span class="sxs-lookup"><span data-stu-id="0c9bc-118">OUTPUTS</span></span>

### <span data-ttu-id="0c9bc-119">RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="0c9bc-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="0c9bc-120">筆記</span><span class="sxs-lookup"><span data-stu-id="0c9bc-120">NOTES</span></span>

## <span data-ttu-id="0c9bc-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c9bc-121">RELATED LINKS</span></span>
