---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 48454b3b6bda283763b05657b0bc652fa9973233
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135462"
---
# <span data-ttu-id="4d27a-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="4d27a-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="4d27a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4d27a-102">SYNOPSIS</span></span>

<span data-ttu-id="4d27a-103">設定電子倉庫內容。</span><span class="sxs-lookup"><span data-stu-id="4d27a-103">Sets vault context.</span></span>

## <span data-ttu-id="4d27a-104">句法</span><span class="sxs-lookup"><span data-stu-id="4d27a-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d27a-105">說明</span><span class="sxs-lookup"><span data-stu-id="4d27a-105">DESCRIPTION</span></span>

<span data-ttu-id="4d27a-106">**AzRecoveryServicesVaultCoNtext** Cmdlet 會設定 Azure Site Recovery 服務的保存庫內容。</span><span class="sxs-lookup"><span data-stu-id="4d27a-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="4d27a-107">警告：此 Cmdlet 在未來的重大變更發行中已被棄用。</span><span class="sxs-lookup"><span data-stu-id="4d27a-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="4d27a-108">它不會取代。</span><span class="sxs-lookup"><span data-stu-id="4d27a-108">There will be no replacement for it.</span></span> <span data-ttu-id="4d27a-109">請在轉寄的所有復原服務命令中使用-VaultId 參數。</span><span class="sxs-lookup"><span data-stu-id="4d27a-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="4d27a-110">示例</span><span class="sxs-lookup"><span data-stu-id="4d27a-110">EXAMPLES</span></span>

### <span data-ttu-id="4d27a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4d27a-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="4d27a-112">設定電子倉庫內容。</span><span class="sxs-lookup"><span data-stu-id="4d27a-112">Sets vault context.</span></span>

## <span data-ttu-id="4d27a-113">參數</span><span class="sxs-lookup"><span data-stu-id="4d27a-113">PARAMETERS</span></span>

### <span data-ttu-id="4d27a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d27a-114">-DefaultProfile</span></span>

<span data-ttu-id="4d27a-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4d27a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d27a-116">-保存庫</span><span class="sxs-lookup"><span data-stu-id="4d27a-116">-Vault</span></span>

<span data-ttu-id="4d27a-117">指定保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d27a-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="4d27a-118">Vault 必須是 **AzureRmRecoveryServicesVault** 物件。</span><span class="sxs-lookup"><span data-stu-id="4d27a-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="4d27a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d27a-119">CommonParameters</span></span>
<span data-ttu-id="4d27a-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4d27a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d27a-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4d27a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d27a-122">輸入</span><span class="sxs-lookup"><span data-stu-id="4d27a-122">INPUTS</span></span>

### <span data-ttu-id="4d27a-123">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4d27a-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="4d27a-124">輸出</span><span class="sxs-lookup"><span data-stu-id="4d27a-124">OUTPUTS</span></span>

### <span data-ttu-id="4d27a-125">System.void</span><span class="sxs-lookup"><span data-stu-id="4d27a-125">System.Void</span></span>

## <span data-ttu-id="4d27a-126">筆記</span><span class="sxs-lookup"><span data-stu-id="4d27a-126">NOTES</span></span>

## <span data-ttu-id="4d27a-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="4d27a-127">RELATED LINKS</span></span>