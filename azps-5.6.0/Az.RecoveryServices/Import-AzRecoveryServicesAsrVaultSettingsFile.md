---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/import-azrecoveryservicesasrvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Import-AzRecoveryServicesAsrVaultSettingsFile.md
ms.openlocfilehash: b287e69093ca748d02cd3f630e3b38fb51cdf8f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916373"
---
# <span data-ttu-id="5c449-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="5c449-101">Import-AzRecoveryServicesAsrVaultSettingsFile</span></span>

## <span data-ttu-id="5c449-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5c449-102">SYNOPSIS</span></span>
<span data-ttu-id="5c449-103">將指定的 ASR 保存庫設定檔案， (PowerShell 會話上下文的保存庫上下文設定) PowerShell 會話中後續的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="5c449-103">Imports the specified ASR vault settings file to set the vault context(PowerShell session context) for subsequent ASR operations in the PowerShell session.</span></span> 

## <span data-ttu-id="5c449-104">語法</span><span class="sxs-lookup"><span data-stu-id="5c449-104">SYNTAX</span></span>

```
Import-AzRecoveryServicesAsrVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c449-105">描述</span><span class="sxs-lookup"><span data-stu-id="5c449-105">DESCRIPTION</span></span>
<span data-ttu-id="5c449-106">**Import-AzRecoveryServicesAsrVaultSettingsFile** Cmdlet 會導入 Azure 網站復原保存庫設定檔案。</span><span class="sxs-lookup"><span data-stu-id="5c449-106">The **Import-AzRecoveryServicesAsrVaultSettingsFile** cmdlet imports the Azure Site Recovery vault settings file.</span></span> <span data-ttu-id="5c449-107">保存庫設定檔案用來設定目前會話中後續 Azure 網站復原作業的保存庫上下文。</span><span class="sxs-lookup"><span data-stu-id="5c449-107">The vault settings file is used to set the vault context for subsequent Azure Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="5c449-108">例子</span><span class="sxs-lookup"><span data-stu-id="5c449-108">EXAMPLES</span></span>

### <span data-ttu-id="5c449-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="5c449-109">Example 1</span></span>
```
PS C:\> $VaultSettings = Import-AzRecoveryServicesAsrVaultSettingsFile -Path $FilePath
```

<span data-ttu-id="5c449-110">匯出指定的修復服務保存庫設定檔案，並返回所輸入保存庫的設定。</span><span class="sxs-lookup"><span data-stu-id="5c449-110">Imports the specified Recovery Services vault settings file and returns settings of the imported vault.</span></span>

## <span data-ttu-id="5c449-111">參數</span><span class="sxs-lookup"><span data-stu-id="5c449-111">PARAMETERS</span></span>

### <span data-ttu-id="5c449-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c449-112">-DefaultProfile</span></span>
<span data-ttu-id="5c449-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c449-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5c449-114">-路徑</span><span class="sxs-lookup"><span data-stu-id="5c449-114">-Path</span></span>
<span data-ttu-id="5c449-115">指定 ASR 保存庫設定檔案的資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="5c449-115">Specifies the folder path of the ASR vault settings file.</span></span>
<span data-ttu-id="5c449-116">此檔案可以從修復服務保存庫入口網站下載，並儲存在本地。</span><span class="sxs-lookup"><span data-stu-id="5c449-116">This file can be downloaded from the Recovery Services vault portal and stored locally.</span></span>

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

### <span data-ttu-id="5c449-117">-確認</span><span class="sxs-lookup"><span data-stu-id="5c449-117">-Confirm</span></span>
<span data-ttu-id="5c449-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5c449-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c449-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c449-119">-WhatIf</span></span>
<span data-ttu-id="5c449-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5c449-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c449-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c449-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c449-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c449-122">CommonParameters</span></span>
<span data-ttu-id="5c449-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5c449-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c449-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c449-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c449-125">輸入</span><span class="sxs-lookup"><span data-stu-id="5c449-125">INPUTS</span></span>

### <span data-ttu-id="5c449-126">System.String</span><span class="sxs-lookup"><span data-stu-id="5c449-126">System.String</span></span>

## <span data-ttu-id="5c449-127">輸出</span><span class="sxs-lookup"><span data-stu-id="5c449-127">OUTPUTS</span></span>

### <span data-ttu-id="5c449-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="5c449-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="5c449-129">筆記</span><span class="sxs-lookup"><span data-stu-id="5c449-129">NOTES</span></span>

## <span data-ttu-id="5c449-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c449-130">RELATED LINKS</span></span>

[<span data-ttu-id="5c449-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="5c449-131">Get-AzRecoveryServicesAsrVaultSettingsFile</span></span>](./Get-AzRecoveryServicesAsrVaultSettingsFile.md)
