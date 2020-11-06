---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/remove-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 4d3046827a7d3338833b0c8c788cfb7a9e18bc2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452096"
---
# <span data-ttu-id="a1a76-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a1a76-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="a1a76-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1a76-102">SYNOPSIS</span></span>
<span data-ttu-id="a1a76-103">刪除恢復服務電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="a1a76-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1a76-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1a76-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1a76-105">說明</span><span class="sxs-lookup"><span data-stu-id="a1a76-105">DESCRIPTION</span></span>
<span data-ttu-id="a1a76-106">**AzureRmRecoveryServicesVault** Cmdlet 會刪除 [恢復服務] 保存庫。</span><span class="sxs-lookup"><span data-stu-id="a1a76-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="a1a76-107">示例</span><span class="sxs-lookup"><span data-stu-id="a1a76-107">EXAMPLES</span></span>

### <span data-ttu-id="a1a76-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a1a76-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="a1a76-109">刪除恢復服務電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="a1a76-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="a1a76-110">參數</span><span class="sxs-lookup"><span data-stu-id="a1a76-110">PARAMETERS</span></span>

### <span data-ttu-id="a1a76-111">-保存庫</span><span class="sxs-lookup"><span data-stu-id="a1a76-111">-Vault</span></span>
<span data-ttu-id="a1a76-112">指定 Azure Site Recovery 保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="a1a76-112">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="a1a76-113">-確認</span><span class="sxs-lookup"><span data-stu-id="a1a76-113">-Confirm</span></span>
<span data-ttu-id="a1a76-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a1a76-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1a76-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1a76-115">-WhatIf</span></span>
<span data-ttu-id="a1a76-116">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a1a76-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1a76-117">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a1a76-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1a76-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1a76-118">-DefaultProfile</span></span>
<span data-ttu-id="a1a76-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1a76-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1a76-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1a76-120">CommonParameters</span></span>
<span data-ttu-id="a1a76-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1a76-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1a76-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a1a76-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1a76-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a1a76-123">INPUTS</span></span>

### <span data-ttu-id="a1a76-124">ARSVault</span><span class="sxs-lookup"><span data-stu-id="a1a76-124">ARSVault</span></span>
<span data-ttu-id="a1a76-125">參數 "Vault" 接受來自管線的 "ARSVault" 類型值</span><span class="sxs-lookup"><span data-stu-id="a1a76-125">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="a1a76-126">輸出</span><span class="sxs-lookup"><span data-stu-id="a1a76-126">OUTPUTS</span></span>

### <span data-ttu-id="a1a76-127">VaultOperationOutput 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a1a76-127">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="a1a76-128">筆記</span><span class="sxs-lookup"><span data-stu-id="a1a76-128">NOTES</span></span>

## <span data-ttu-id="a1a76-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1a76-129">RELATED LINKS</span></span>

[<span data-ttu-id="a1a76-130">AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a1a76-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="a1a76-131">AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="a1a76-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="a1a76-132">新-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a1a76-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


