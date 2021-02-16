---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: f71f7e37e4864de10c5387d63c101cd66ed9fd34
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412617"
---
# <span data-ttu-id="9f4aa-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="9f4aa-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="9f4aa-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9f4aa-102">SYNOPSIS</span></span>
<span data-ttu-id="9f4aa-103">將指定的 ASR 保存庫設定檔案， (PowerShell 會話上下文的保存庫上下文設定) PowerShell 會話中後續的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="9f4aa-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="9f4aa-104">語法</span><span class="sxs-lookup"><span data-stu-id="9f4aa-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f4aa-105">描述</span><span class="sxs-lookup"><span data-stu-id="9f4aa-105">DESCRIPTION</span></span>
<span data-ttu-id="9f4aa-106">**Import-AzRecoveryServicesAsrVaultSettingsFile** Cmdlet 會導入 Azure 網站復原保存庫設定檔案。</span><span class="sxs-lookup"><span data-stu-id="9f4aa-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="9f4aa-107">保存庫設定檔案用來設定目前會話中後續 Azure 網站復原作業的保存庫上下文。</span><span class="sxs-lookup"><span data-stu-id="9f4aa-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="9f4aa-108">例子</span><span class="sxs-lookup"><span data-stu-id="9f4aa-108">EXAMPLES</span></span>

### <span data-ttu-id="9f4aa-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="9f4aa-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="9f4aa-110">匯出指定的修復服務保存庫設定檔案，並返回所導入保存庫的設定。</span><span class="sxs-lookup"><span data-stu-id="9f4aa-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="9f4aa-111">參數</span><span class="sxs-lookup"><span data-stu-id="9f4aa-111">PARAMETERS</span></span>

### <span data-ttu-id="9f4aa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f4aa-112">-DefaultProfile</span></span>
<span data-ttu-id="9f4aa-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9f4aa-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9f4aa-114">-路徑</span><span class="sxs-lookup"><span data-stu-id="9f4aa-114">-Path</span></span>
<span data-ttu-id="9f4aa-115">指定 ASR 保存庫設定檔案的資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="9f4aa-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="9f4aa-116">此檔案可以從修復服務保存庫入口網站下載，並儲存在本地。</span><span class="sxs-lookup"><span data-stu-id="9f4aa-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="9f4aa-117">-確認</span><span class="sxs-lookup"><span data-stu-id="9f4aa-117">-Confirm</span></span>
<span data-ttu-id="9f4aa-118">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9f4aa-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f4aa-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f4aa-119">-WhatIf</span></span>
<span data-ttu-id="9f4aa-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9f4aa-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f4aa-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9f4aa-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f4aa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f4aa-122">CommonParameters</span></span>
<span data-ttu-id="9f4aa-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9f4aa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f4aa-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f4aa-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f4aa-125">輸入</span><span class="sxs-lookup"><span data-stu-id="9f4aa-125">INPUTS</span></span>

### <span data-ttu-id="9f4aa-126">System.String</span><span class="sxs-lookup"><span data-stu-id="9f4aa-126">System.String</span></span>

## <span data-ttu-id="9f4aa-127">輸出</span><span class="sxs-lookup"><span data-stu-id="9f4aa-127">OUTPUTS</span></span>

### <span data-ttu-id="9f4aa-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="9f4aa-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="9f4aa-129">筆記</span><span class="sxs-lookup"><span data-stu-id="9f4aa-129">NOTES</span></span>

## <span data-ttu-id="9f4aa-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="9f4aa-130">RELATED LINKS</span></span>

