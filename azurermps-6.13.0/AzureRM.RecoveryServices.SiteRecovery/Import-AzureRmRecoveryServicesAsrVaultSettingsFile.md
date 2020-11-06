---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/import-azurermrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Import-AzureRmRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: 7bb92a55f366d90eb5993cfe1520d1b516214372
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445575"
---
# <span data-ttu-id="925bc-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="925bc-101">Import-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="925bc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="925bc-102">SYNOPSIS</span></span>
<span data-ttu-id="925bc-103">匯入指定的 ASR 電子倉庫設定檔案，以便在 PowerShell 會話中針對後續的 ASR 作業 (PowerShell 會話內容) 設定 vault 內容。</span><span class="sxs-lookup"><span data-stu-id="925bc-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="925bc-104">句法</span><span class="sxs-lookup"><span data-stu-id="925bc-104">SYNTAX</span></span>

```
Import-AzureRmRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="925bc-105">說明</span><span class="sxs-lookup"><span data-stu-id="925bc-105">DESCRIPTION</span></span>
<span data-ttu-id="925bc-106">匯 **入-AzureRmRecoveryServicesAsrVaultSettingsFile** Cmdlet 會匯入 Azure Site Recovery 保存庫設定檔。</span><span class="sxs-lookup"><span data-stu-id="925bc-106">The **Import-AzureRmRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="925bc-107">Vault 設定檔案是用來在目前的會話中設定後續 Azure 網站恢復作業的保存庫內容。</span><span class="sxs-lookup"><span data-stu-id="925bc-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="925bc-108">示例</span><span class="sxs-lookup"><span data-stu-id="925bc-108">EXAMPLES</span></span>

### <span data-ttu-id="925bc-109">範例1</span><span class="sxs-lookup"><span data-stu-id="925bc-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzureRmRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="925bc-110">匯入指定的復原服務電子倉庫設定檔案，並傳回已匯入的電子倉庫的設定。</span><span class="sxs-lookup"><span data-stu-id="925bc-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="925bc-111">參數</span><span class="sxs-lookup"><span data-stu-id="925bc-111">PARAMETERS</span></span>

### <span data-ttu-id="925bc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="925bc-112">-DefaultProfile</span></span>
<span data-ttu-id="925bc-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="925bc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="925bc-114">-Path</span><span class="sxs-lookup"><span data-stu-id="925bc-114">-Path</span></span>
<span data-ttu-id="925bc-115">指定 ASR 電子倉庫設定檔案的資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="925bc-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="925bc-116">此檔案可從 [恢復服務] vault 入口網站下載，並儲存在本機。</span><span class="sxs-lookup"><span data-stu-id="925bc-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="925bc-117">-確認</span><span class="sxs-lookup"><span data-stu-id="925bc-117">-Confirm</span></span>
<span data-ttu-id="925bc-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="925bc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="925bc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="925bc-119">-WhatIf</span></span>
<span data-ttu-id="925bc-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="925bc-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="925bc-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="925bc-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="925bc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="925bc-122">CommonParameters</span></span>
<span data-ttu-id="925bc-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="925bc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="925bc-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="925bc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="925bc-125">輸入</span><span class="sxs-lookup"><span data-stu-id="925bc-125">INPUTS</span></span>

### <span data-ttu-id="925bc-126">System.object</span><span class="sxs-lookup"><span data-stu-id="925bc-126">System.String</span></span>

## <span data-ttu-id="925bc-127">輸出</span><span class="sxs-lookup"><span data-stu-id="925bc-127">OUTPUTS</span></span>

### <span data-ttu-id="925bc-128">RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="925bc-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="925bc-129">筆記</span><span class="sxs-lookup"><span data-stu-id="925bc-129">NOTES</span></span>

## <span data-ttu-id="925bc-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="925bc-130">RELATED LINKS</span></span>

[<span data-ttu-id="925bc-131">AzureRmRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="925bc-131">Get-AzureRmRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesAsrVaultSettingsFile.md)
