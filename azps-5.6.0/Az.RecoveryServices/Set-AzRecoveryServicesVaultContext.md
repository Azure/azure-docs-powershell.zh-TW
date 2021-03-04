---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 04fa3c9a7024b8a9e1f525a4ef131ae151f25804
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913737"
---
# <span data-ttu-id="9986c-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="9986c-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="9986c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9986c-102">SYNOPSIS</span></span>

<span data-ttu-id="9986c-103">設定儲存庫內容。</span><span class="sxs-lookup"><span data-stu-id="9986c-103">Sets vault context.</span></span>

## <span data-ttu-id="9986c-104">語法</span><span class="sxs-lookup"><span data-stu-id="9986c-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9986c-105">描述</span><span class="sxs-lookup"><span data-stu-id="9986c-105">DESCRIPTION</span></span>

<span data-ttu-id="9986c-106">**Set-AzRecoveryServicesVaultCoNtext** Cmdlet 會設定 Azure 網站復原服務的庫上下文。</span><span class="sxs-lookup"><span data-stu-id="9986c-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="9986c-107">警告：此 Cmdlet 在未來中斷的變更版本中已遭到使用。</span><span class="sxs-lookup"><span data-stu-id="9986c-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="9986c-108">此產品將無法取代。</span><span class="sxs-lookup"><span data-stu-id="9986c-108">There will be no replacement for it.</span></span> <span data-ttu-id="9986c-109">請未來在所有修復服務命令中使用 -VaultId 參數。</span><span class="sxs-lookup"><span data-stu-id="9986c-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="9986c-110">例子</span><span class="sxs-lookup"><span data-stu-id="9986c-110">EXAMPLES</span></span>

### <span data-ttu-id="9986c-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="9986c-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="9986c-112">設定儲存庫內容。</span><span class="sxs-lookup"><span data-stu-id="9986c-112">Sets vault context.</span></span>

## <span data-ttu-id="9986c-113">參數</span><span class="sxs-lookup"><span data-stu-id="9986c-113">PARAMETERS</span></span>

### <span data-ttu-id="9986c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9986c-114">-DefaultProfile</span></span>

<span data-ttu-id="9986c-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9986c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9986c-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="9986c-116">-Vault</span></span>

<span data-ttu-id="9986c-117">指定儲存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="9986c-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="9986c-118">該庫必須是 **AzureRmRecoveryServicesVault** 物件。</span><span class="sxs-lookup"><span data-stu-id="9986c-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="9986c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9986c-119">CommonParameters</span></span>
<span data-ttu-id="9986c-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9986c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9986c-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9986c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9986c-122">輸入</span><span class="sxs-lookup"><span data-stu-id="9986c-122">INPUTS</span></span>

### <span data-ttu-id="9986c-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="9986c-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="9986c-124">輸出</span><span class="sxs-lookup"><span data-stu-id="9986c-124">OUTPUTS</span></span>

### <span data-ttu-id="9986c-125">System.Void</span><span class="sxs-lookup"><span data-stu-id="9986c-125">System.Void</span></span>

## <span data-ttu-id="9986c-126">筆記</span><span class="sxs-lookup"><span data-stu-id="9986c-126">NOTES</span></span>

## <span data-ttu-id="9986c-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="9986c-127">RELATED LINKS</span></span>
