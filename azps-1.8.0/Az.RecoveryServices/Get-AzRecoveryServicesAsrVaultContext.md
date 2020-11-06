---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: e5bb8a19cb616c9696ec224d8f1d9d25678d9e47
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621163"
---
# <span data-ttu-id="f80a9-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="f80a9-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="f80a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f80a9-102">SYNOPSIS</span></span>
<span data-ttu-id="f80a9-103">取得恢復服務電子倉庫的 ASR vault 設定資訊。</span><span class="sxs-lookup"><span data-stu-id="f80a9-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="f80a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="f80a9-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f80a9-105">說明</span><span class="sxs-lookup"><span data-stu-id="f80a9-105">DESCRIPTION</span></span>
<span data-ttu-id="f80a9-106">**AzRecoveryServicesAsrVaultCoNtext** Cmdlet 會取得與 [恢復服務] 保存庫相關的 ASR vault 設定資訊。</span><span class="sxs-lookup"><span data-stu-id="f80a9-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="f80a9-107">示例</span><span class="sxs-lookup"><span data-stu-id="f80a9-107">EXAMPLES</span></span>

### <span data-ttu-id="f80a9-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f80a9-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="f80a9-109">取得 PowerShell 會話) 復原服務電子倉庫中目前作用中 (的 ASR vault 設定。</span><span class="sxs-lookup"><span data-stu-id="f80a9-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="f80a9-110">參數</span><span class="sxs-lookup"><span data-stu-id="f80a9-110">PARAMETERS</span></span>

### <span data-ttu-id="f80a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f80a9-111">-DefaultProfile</span></span>
<span data-ttu-id="f80a9-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f80a9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f80a9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f80a9-113">CommonParameters</span></span>
<span data-ttu-id="f80a9-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f80a9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f80a9-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f80a9-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f80a9-116">輸入</span><span class="sxs-lookup"><span data-stu-id="f80a9-116">INPUTS</span></span>

### <span data-ttu-id="f80a9-117">所有</span><span class="sxs-lookup"><span data-stu-id="f80a9-117">None</span></span>

## <span data-ttu-id="f80a9-118">輸出</span><span class="sxs-lookup"><span data-stu-id="f80a9-118">OUTPUTS</span></span>

### <span data-ttu-id="f80a9-119">RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="f80a9-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="f80a9-120">筆記</span><span class="sxs-lookup"><span data-stu-id="f80a9-120">NOTES</span></span>

## <span data-ttu-id="f80a9-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="f80a9-121">RELATED LINKS</span></span>
