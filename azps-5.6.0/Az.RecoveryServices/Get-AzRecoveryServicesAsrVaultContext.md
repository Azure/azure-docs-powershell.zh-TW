---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 62f27b43158f8b01abc7be48cab93f4bb957258b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903442"
---
# <span data-ttu-id="2c1ee-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="2c1ee-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="2c1ee-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2c1ee-102">SYNOPSIS</span></span>
<span data-ttu-id="2c1ee-103">獲得修復服務保存庫的 ASR 保存庫設定資訊。</span><span class="sxs-lookup"><span data-stu-id="2c1ee-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="2c1ee-104">語法</span><span class="sxs-lookup"><span data-stu-id="2c1ee-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c1ee-105">描述</span><span class="sxs-lookup"><span data-stu-id="2c1ee-105">DESCRIPTION</span></span>
<span data-ttu-id="2c1ee-106">**Get-AzRecoveryServicesAsrVaultCoNtext** Cmdlet 會取得與修復服務保存庫相關的 ASR 保存庫設定資訊。</span><span class="sxs-lookup"><span data-stu-id="2c1ee-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="2c1ee-107">例子</span><span class="sxs-lookup"><span data-stu-id="2c1ee-107">EXAMPLES</span></span>

### <span data-ttu-id="2c1ee-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="2c1ee-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="2c1ee-109">在 PowerShell 會話或復原服務保存庫中， (作用中) 的 ASR 保存庫設定。</span><span class="sxs-lookup"><span data-stu-id="2c1ee-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="2c1ee-110">參數</span><span class="sxs-lookup"><span data-stu-id="2c1ee-110">PARAMETERS</span></span>

### <span data-ttu-id="2c1ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c1ee-111">-DefaultProfile</span></span>
<span data-ttu-id="2c1ee-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c1ee-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c1ee-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c1ee-113">CommonParameters</span></span>
<span data-ttu-id="2c1ee-114">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2c1ee-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c1ee-115">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c1ee-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c1ee-116">輸入</span><span class="sxs-lookup"><span data-stu-id="2c1ee-116">INPUTS</span></span>

### <span data-ttu-id="2c1ee-117">沒有</span><span class="sxs-lookup"><span data-stu-id="2c1ee-117">None</span></span>

## <span data-ttu-id="2c1ee-118">輸出</span><span class="sxs-lookup"><span data-stu-id="2c1ee-118">OUTPUTS</span></span>

### <span data-ttu-id="2c1ee-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="2c1ee-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="2c1ee-120">筆記</span><span class="sxs-lookup"><span data-stu-id="2c1ee-120">NOTES</span></span>

## <span data-ttu-id="2c1ee-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c1ee-121">RELATED LINKS</span></span>
