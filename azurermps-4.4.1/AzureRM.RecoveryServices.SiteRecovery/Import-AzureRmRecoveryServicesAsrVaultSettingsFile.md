---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: ad22cbe1cb17e69358ef386b478fe929abe415b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623871"
---
# <span data-ttu-id="2afe0-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="2afe0-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="2afe0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2afe0-102">SYNOPSIS</span></span>
<span data-ttu-id="2afe0-103">匯入指定的 ASR 電子倉庫設定檔案，以便在 PowerShell 會話中針對後續的 ASR 作業 (PowerShell 會話內容) 設定 vault 內容。</span><span class="sxs-lookup"><span data-stu-id="2afe0-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2afe0-104">句法</span><span class="sxs-lookup"><span data-stu-id="2afe0-104">SYNTAX</span></span>

```
Import-AzureRmRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2afe0-105">說明</span><span class="sxs-lookup"><span data-stu-id="2afe0-105">DESCRIPTION</span></span>
<span data-ttu-id="2afe0-106">匯 **入-AzureRmRecoveryServicesAsrVaultSettingsFile** Cmdlet 會匯入 Azure Site Recovery 保存庫設定檔。</span><span class="sxs-lookup"><span data-stu-id="2afe0-106">The **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="2afe0-107">Vault 設定檔案是用來在目前的會話中設定後續 Azure 網站恢復作業的保存庫內容。</span><span class="sxs-lookup"><span data-stu-id="2afe0-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="2afe0-108">示例</span><span class="sxs-lookup"><span data-stu-id="2afe0-108">EXAMPLES</span></span>

### <span data-ttu-id="2afe0-109">範例1</span><span class="sxs-lookup"><span data-stu-id="2afe0-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzureRmRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="2afe0-110">匯入指定的復原服務電子倉庫設定檔案，並傳回已匯入的電子倉庫的設定。</span><span class="sxs-lookup"><span data-stu-id="2afe0-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="2afe0-111">參數</span><span class="sxs-lookup"><span data-stu-id="2afe0-111">PARAMETERS</span></span>

### <span data-ttu-id="2afe0-112">-Path</span><span class="sxs-lookup"><span data-stu-id="2afe0-112">-Path</span></span>
<span data-ttu-id="2afe0-113">指定 ASR vault 設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="2afe0-113">Specifies the path of the ASR vault settings file.</span></span>
<span data-ttu-id="2afe0-114">此檔案可從 [恢復服務] vault 入口網站下載，並儲存在本機。</span><span class="sxs-lookup"><span data-stu-id="2afe0-114">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2afe0-115">-確認</span><span class="sxs-lookup"><span data-stu-id="2afe0-115">-Confirm</span></span>
<span data-ttu-id="2afe0-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2afe0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2afe0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2afe0-117">-WhatIf</span></span>
<span data-ttu-id="2afe0-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2afe0-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2afe0-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2afe0-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2afe0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2afe0-120">CommonParameters</span></span>
<span data-ttu-id="2afe0-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2afe0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2afe0-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2afe0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2afe0-123">輸入</span><span class="sxs-lookup"><span data-stu-id="2afe0-123">INPUTS</span></span>

### <span data-ttu-id="2afe0-124">System.object</span><span class="sxs-lookup"><span data-stu-id="2afe0-124">System.String</span></span>

## <span data-ttu-id="2afe0-125">輸出</span><span class="sxs-lookup"><span data-stu-id="2afe0-125">OUTPUTS</span></span>

### <span data-ttu-id="2afe0-126">RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="2afe0-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="2afe0-127">筆記</span><span class="sxs-lookup"><span data-stu-id="2afe0-127">NOTES</span></span>

## <span data-ttu-id="2afe0-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="2afe0-128">RELATED LINKS</span></span>

[<span data-ttu-id="2afe0-129">AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="2afe0-129">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesAsrVaultSettingsFile.md)
