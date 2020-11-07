---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: b3df84865d29bbcf62074c1b1ed7f5586fb64fee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625086"
---
# <span data-ttu-id="17bf3-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="17bf3-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="17bf3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="17bf3-102">SYNOPSIS</span></span>
<span data-ttu-id="17bf3-103">刪除恢復服務電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="17bf3-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17bf3-104">句法</span><span class="sxs-lookup"><span data-stu-id="17bf3-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17bf3-105">說明</span><span class="sxs-lookup"><span data-stu-id="17bf3-105">DESCRIPTION</span></span>
<span data-ttu-id="17bf3-106">**AzureRmRecoveryServicesVault** Cmdlet 會刪除 [恢復服務] 保存庫。</span><span class="sxs-lookup"><span data-stu-id="17bf3-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="17bf3-107">示例</span><span class="sxs-lookup"><span data-stu-id="17bf3-107">EXAMPLES</span></span>

## <span data-ttu-id="17bf3-108">參數</span><span class="sxs-lookup"><span data-stu-id="17bf3-108">PARAMETERS</span></span>

### <span data-ttu-id="17bf3-109">-保存庫</span><span class="sxs-lookup"><span data-stu-id="17bf3-109">-Vault</span></span>
<span data-ttu-id="17bf3-110">指定 Azure Site Recovery 保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="17bf3-110">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="17bf3-111">-確認</span><span class="sxs-lookup"><span data-stu-id="17bf3-111">-Confirm</span></span>
<span data-ttu-id="17bf3-112">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="17bf3-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17bf3-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17bf3-113">-WhatIf</span></span>
<span data-ttu-id="17bf3-114">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="17bf3-114">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17bf3-115">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="17bf3-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17bf3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17bf3-116">-DefaultProfile</span></span>
<span data-ttu-id="17bf3-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="17bf3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17bf3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17bf3-118">CommonParameters</span></span>
<span data-ttu-id="17bf3-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="17bf3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17bf3-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="17bf3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17bf3-121">輸入</span><span class="sxs-lookup"><span data-stu-id="17bf3-121">INPUTS</span></span>

### <span data-ttu-id="17bf3-122">ARSVault</span><span class="sxs-lookup"><span data-stu-id="17bf3-122">ARSVault</span></span>
<span data-ttu-id="17bf3-123">參數 "Vault" 接受來自管線的 "ARSVault" 類型值</span><span class="sxs-lookup"><span data-stu-id="17bf3-123">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="17bf3-124">輸出</span><span class="sxs-lookup"><span data-stu-id="17bf3-124">OUTPUTS</span></span>

### <span data-ttu-id="17bf3-125">VaultOperationOutput 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="17bf3-125">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="17bf3-126">筆記</span><span class="sxs-lookup"><span data-stu-id="17bf3-126">NOTES</span></span>

## <span data-ttu-id="17bf3-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="17bf3-127">RELATED LINKS</span></span>

[<span data-ttu-id="17bf3-128">AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="17bf3-128">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="17bf3-129">AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="17bf3-129">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="17bf3-130">新-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="17bf3-130">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


