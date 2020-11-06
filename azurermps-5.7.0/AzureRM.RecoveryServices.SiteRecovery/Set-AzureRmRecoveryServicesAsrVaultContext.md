---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: c85d372ccd17b23fec46655245d050b668a32dc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448599"
---
# <span data-ttu-id="dcbdb-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="dcbdb-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="dcbdb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dcbdb-102">SYNOPSIS</span></span>
<span data-ttu-id="dcbdb-103">設定要用於在目前 PowerShell 會話中進行後續 Azure 網站恢復作業的復原服務電子倉庫內容。</span><span class="sxs-lookup"><span data-stu-id="dcbdb-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcbdb-104">句法</span><span class="sxs-lookup"><span data-stu-id="dcbdb-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcbdb-105">說明</span><span class="sxs-lookup"><span data-stu-id="dcbdb-105">DESCRIPTION</span></span>
<span data-ttu-id="dcbdb-106">**AzureRmRecoveryServicesAsrVaultCoNtext** Cmdlet 會設定 Azure Site Recovery 保存庫內容以進行進一步的操作。</span><span class="sxs-lookup"><span data-stu-id="dcbdb-106">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="dcbdb-107">示例</span><span class="sxs-lookup"><span data-stu-id="dcbdb-107">EXAMPLES</span></span>

### <span data-ttu-id="dcbdb-108">範例1</span><span class="sxs-lookup"><span data-stu-id="dcbdb-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="dcbdb-109">在目前的 PowerShell 會話中，將保存庫內容設為指定的 [恢復服務] 保存庫，以進行後續的 Azure 網站恢復作業。</span><span class="sxs-lookup"><span data-stu-id="dcbdb-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="dcbdb-110">參數</span><span class="sxs-lookup"><span data-stu-id="dcbdb-110">PARAMETERS</span></span>

### <span data-ttu-id="dcbdb-111">-確認</span><span class="sxs-lookup"><span data-stu-id="dcbdb-111">-Confirm</span></span>
<span data-ttu-id="dcbdb-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dcbdb-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcbdb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcbdb-113">-DefaultProfile</span></span>
<span data-ttu-id="dcbdb-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dcbdb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcbdb-115">-保存庫</span><span class="sxs-lookup"><span data-stu-id="dcbdb-115">-Vault</span></span>
<span data-ttu-id="dcbdb-116">與 [恢復服務] 保存庫相對應的 [恢復服務] 保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="dcbdb-116">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcbdb-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcbdb-117">-WhatIf</span></span>
<span data-ttu-id="dcbdb-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dcbdb-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcbdb-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dcbdb-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcbdb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcbdb-120">CommonParameters</span></span>
<span data-ttu-id="dcbdb-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dcbdb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcbdb-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dcbdb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcbdb-123">輸入</span><span class="sxs-lookup"><span data-stu-id="dcbdb-123">INPUTS</span></span>

### <span data-ttu-id="dcbdb-124">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="dcbdb-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="dcbdb-125">輸出</span><span class="sxs-lookup"><span data-stu-id="dcbdb-125">OUTPUTS</span></span>

### <span data-ttu-id="dcbdb-126">RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="dcbdb-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="dcbdb-127">筆記</span><span class="sxs-lookup"><span data-stu-id="dcbdb-127">NOTES</span></span>

## <span data-ttu-id="dcbdb-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="dcbdb-128">RELATED LINKS</span></span>
