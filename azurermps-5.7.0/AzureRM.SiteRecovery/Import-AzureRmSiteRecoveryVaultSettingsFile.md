---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 070DA86E-9EA4-4777-9D53-64B58B4401B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/import-azurermsiterecoveryvaultsettingsfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 11233414250377331f75e3e8b69f262a0f3a0537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454035"
---
# <span data-ttu-id="21334-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="21334-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="21334-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21334-102">SYNOPSIS</span></span>
<span data-ttu-id="21334-103">匯入網站復原電子倉庫設定檔。</span><span class="sxs-lookup"><span data-stu-id="21334-103">Imports a Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21334-104">句法</span><span class="sxs-lookup"><span data-stu-id="21334-104">SYNTAX</span></span>

```
Import-AzureRmSiteRecoveryVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21334-105">說明</span><span class="sxs-lookup"><span data-stu-id="21334-105">DESCRIPTION</span></span>
<span data-ttu-id="21334-106">匯 **入-AzureRmSiteRecoveryVaultSettingsFile** Cmdlet 會匯入 Azure Site Recovery 保存庫設定檔案，以在目前的會話中設定後續網站恢復作業的保存庫內容。</span><span class="sxs-lookup"><span data-stu-id="21334-106">The **Import-AzureRmSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="21334-107">示例</span><span class="sxs-lookup"><span data-stu-id="21334-107">EXAMPLES</span></span>

## <span data-ttu-id="21334-108">參數</span><span class="sxs-lookup"><span data-stu-id="21334-108">PARAMETERS</span></span>

### <span data-ttu-id="21334-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21334-109">-DefaultProfile</span></span>
<span data-ttu-id="21334-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21334-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21334-111">-Path</span><span class="sxs-lookup"><span data-stu-id="21334-111">-Path</span></span>
<span data-ttu-id="21334-112">指定網站復原電子倉庫設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="21334-112">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="21334-113">此檔案可以從網站復原電子倉庫入口網站下載，並儲存在本機。</span><span class="sxs-lookup"><span data-stu-id="21334-113">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

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

### <span data-ttu-id="21334-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21334-114">CommonParameters</span></span>
<span data-ttu-id="21334-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21334-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21334-116">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="21334-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21334-117">輸入</span><span class="sxs-lookup"><span data-stu-id="21334-117">INPUTS</span></span>

### <span data-ttu-id="21334-118">所有</span><span class="sxs-lookup"><span data-stu-id="21334-118">None</span></span>
<span data-ttu-id="21334-119">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="21334-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="21334-120">輸出</span><span class="sxs-lookup"><span data-stu-id="21334-120">OUTPUTS</span></span>

### <span data-ttu-id="21334-121">ASRVaultSettings 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="21334-121">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="21334-122">筆記</span><span class="sxs-lookup"><span data-stu-id="21334-122">NOTES</span></span>

## <span data-ttu-id="21334-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="21334-123">RELATED LINKS</span></span>

[<span data-ttu-id="21334-124">AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="21334-124">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureRmSiteRecoveryVaultSettingsFile.md)
