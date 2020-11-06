---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 3d0761ff05a0cdcd775a234b4da0a50d27c2ba08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445555"
---
# <span data-ttu-id="4ca54-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="4ca54-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="4ca54-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ca54-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca54-103">設定要用於在目前 PowerShell 會話中進行後續 Azure 網站恢復作業的復原服務電子倉庫內容。</span><span class="sxs-lookup"><span data-stu-id="4ca54-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ca54-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ca54-104">SYNTAX</span></span>

### <span data-ttu-id="4ca54-105">AzureRecoveryServicesVault (預設) </span><span class="sxs-lookup"><span data-stu-id="4ca54-105">AzureRecoveryServicesVault (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ca54-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4ca54-106">ByResourceId</span></span>
```
Set-AzureRmRecoveryServicesAsrVaultContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ca54-107">說明</span><span class="sxs-lookup"><span data-stu-id="4ca54-107">DESCRIPTION</span></span>
<span data-ttu-id="4ca54-108">**AzureRmRecoveryServicesAsrVaultCoNtext** Cmdlet 會設定 Azure Site Recovery 保存庫內容以進行進一步的操作。</span><span class="sxs-lookup"><span data-stu-id="4ca54-108">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="4ca54-109">示例</span><span class="sxs-lookup"><span data-stu-id="4ca54-109">EXAMPLES</span></span>

### <span data-ttu-id="4ca54-110">範例1</span><span class="sxs-lookup"><span data-stu-id="4ca54-110">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="4ca54-111">在目前的 PowerShell 會話中，將保存庫內容設為指定的 [恢復服務] 保存庫，以進行後續的 Azure 網站恢復作業。</span><span class="sxs-lookup"><span data-stu-id="4ca54-111">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="4ca54-112">參數</span><span class="sxs-lookup"><span data-stu-id="4ca54-112">PARAMETERS</span></span>

### <span data-ttu-id="4ca54-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ca54-113">-DefaultProfile</span></span>
<span data-ttu-id="4ca54-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ca54-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ca54-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ca54-115">-ResourceId</span></span>
<span data-ttu-id="4ca54-116">指定要設定為保存庫內容的 recoveryservices vault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ca54-116">Specifies the recoveryservices vault resource id to be set as Vault context.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ca54-117">-保存庫</span><span class="sxs-lookup"><span data-stu-id="4ca54-117">-Vault</span></span>
<span data-ttu-id="4ca54-118">與 [恢復服務] 保存庫相對應的 [恢復服務] 保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="4ca54-118">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: AzureRecoveryServicesVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ca54-119">-確認</span><span class="sxs-lookup"><span data-stu-id="4ca54-119">-Confirm</span></span>
<span data-ttu-id="4ca54-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4ca54-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ca54-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ca54-121">-WhatIf</span></span>
<span data-ttu-id="4ca54-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4ca54-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ca54-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4ca54-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ca54-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca54-124">CommonParameters</span></span>
<span data-ttu-id="4ca54-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ca54-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ca54-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4ca54-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca54-127">輸入</span><span class="sxs-lookup"><span data-stu-id="4ca54-127">INPUTS</span></span>

### <span data-ttu-id="4ca54-128">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="4ca54-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="4ca54-129">輸出</span><span class="sxs-lookup"><span data-stu-id="4ca54-129">OUTPUTS</span></span>

### <span data-ttu-id="4ca54-130">RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="4ca54-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="4ca54-131">筆記</span><span class="sxs-lookup"><span data-stu-id="4ca54-131">NOTES</span></span>

## <span data-ttu-id="4ca54-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ca54-132">RELATED LINKS</span></span>
