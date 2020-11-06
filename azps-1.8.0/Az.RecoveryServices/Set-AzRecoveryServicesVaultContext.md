---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 4d8839d36bf337e3a710fe31384bb022582a371d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621050"
---
# <span data-ttu-id="beba1-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="beba1-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="beba1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="beba1-102">SYNOPSIS</span></span>
<span data-ttu-id="beba1-103">設定電子倉庫內容。</span><span class="sxs-lookup"><span data-stu-id="beba1-103">Sets vault context.</span></span>

## <span data-ttu-id="beba1-104">句法</span><span class="sxs-lookup"><span data-stu-id="beba1-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="beba1-105">說明</span><span class="sxs-lookup"><span data-stu-id="beba1-105">DESCRIPTION</span></span>
<span data-ttu-id="beba1-106">**AzRecoveryServicesVaultCoNtext** Cmdlet 會設定 Azure Site Recovery 服務的保存庫內容。</span><span class="sxs-lookup"><span data-stu-id="beba1-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="beba1-107">示例</span><span class="sxs-lookup"><span data-stu-id="beba1-107">EXAMPLES</span></span>

### <span data-ttu-id="beba1-108">範例1</span><span class="sxs-lookup"><span data-stu-id="beba1-108">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="beba1-109">設定電子倉庫內容。</span><span class="sxs-lookup"><span data-stu-id="beba1-109">Sets vault context.</span></span>

## <span data-ttu-id="beba1-110">參數</span><span class="sxs-lookup"><span data-stu-id="beba1-110">PARAMETERS</span></span>

### <span data-ttu-id="beba1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beba1-111">-DefaultProfile</span></span>
<span data-ttu-id="beba1-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="beba1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="beba1-113">-保存庫</span><span class="sxs-lookup"><span data-stu-id="beba1-113">-Vault</span></span>
<span data-ttu-id="beba1-114">指定保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="beba1-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="beba1-115">Vault 必須是 **AzureRmRecoveryServicesVault** 物件。</span><span class="sxs-lookup"><span data-stu-id="beba1-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="beba1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beba1-116">CommonParameters</span></span>
<span data-ttu-id="beba1-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="beba1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beba1-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="beba1-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beba1-119">輸入</span><span class="sxs-lookup"><span data-stu-id="beba1-119">INPUTS</span></span>

### <span data-ttu-id="beba1-120">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="beba1-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="beba1-121">輸出</span><span class="sxs-lookup"><span data-stu-id="beba1-121">OUTPUTS</span></span>

### <span data-ttu-id="beba1-122">System.void</span><span class="sxs-lookup"><span data-stu-id="beba1-122">System.Void</span></span>

## <span data-ttu-id="beba1-123">筆記</span><span class="sxs-lookup"><span data-stu-id="beba1-123">NOTES</span></span>

## <span data-ttu-id="beba1-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="beba1-124">RELATED LINKS</span></span>