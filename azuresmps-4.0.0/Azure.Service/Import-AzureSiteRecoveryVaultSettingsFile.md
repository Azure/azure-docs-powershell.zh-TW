---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5875D72D-B8DB-4F72-BF5C-242D40A13DE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5dc0762021db2545b73a9ba7b9d7c53d435ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967706"
---
# <span data-ttu-id="e3c94-101">Import-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e3c94-101">Import-AzureSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="e3c94-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3c94-102">SYNOPSIS</span></span>
<span data-ttu-id="e3c94-103">匯入網站復原電子倉庫設定檔。</span><span class="sxs-lookup"><span data-stu-id="e3c94-103">Imports a Site Recovery vault settings file.</span></span>

## <span data-ttu-id="e3c94-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3c94-104">SYNTAX</span></span>

```
Import-AzureSiteRecoveryVaultSettingsFile -Path <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e3c94-105">說明</span><span class="sxs-lookup"><span data-stu-id="e3c94-105">DESCRIPTION</span></span>
<span data-ttu-id="e3c94-106">匯 **入-AzureSiteRecoveryVaultSettingsFile** Cmdlet 會匯入 Azure Site Recovery 保存庫設定檔案，以在目前的會話中設定後續網站恢復作業的保存庫內容。</span><span class="sxs-lookup"><span data-stu-id="e3c94-106">The **Import-AzureSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="e3c94-107">示例</span><span class="sxs-lookup"><span data-stu-id="e3c94-107">EXAMPLES</span></span>

### <span data-ttu-id="e3c94-108">範例1：匯入電子文件庫設定檔案</span><span class="sxs-lookup"><span data-stu-id="e3c94-108">Example 1: Import a vault settings file</span></span>
```
PS C:\> Import-AzureSiteRecoveryVaultSettingsFile -Path "C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials"
VERBOSE: Vault Settings File path: C:\Users\Contoso\Contosovault Monday, October 6, 2014.VaultCredentials

ResourceName                                                CloudServiceName
------------                                                ----------------
Contosovault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

<span data-ttu-id="e3c94-109">這個命令會將保存庫設定檔案匯入至指定路徑。</span><span class="sxs-lookup"><span data-stu-id="e3c94-109">This command imports the vault settings file at the specified path.</span></span>

## <span data-ttu-id="e3c94-110">參數</span><span class="sxs-lookup"><span data-stu-id="e3c94-110">PARAMETERS</span></span>

### <span data-ttu-id="e3c94-111">-Path</span><span class="sxs-lookup"><span data-stu-id="e3c94-111">-Path</span></span>
<span data-ttu-id="e3c94-112">指定網站復原電子倉庫設定檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="e3c94-112">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="e3c94-113">此檔案可以從網站復原電子倉庫入口網站下載，並儲存在本機。</span><span class="sxs-lookup"><span data-stu-id="e3c94-113">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3c94-114">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e3c94-114">-Profile</span></span>
<span data-ttu-id="e3c94-115">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e3c94-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e3c94-116">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e3c94-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3c94-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3c94-117">CommonParameters</span></span>
<span data-ttu-id="e3c94-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3c94-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3c94-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3c94-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3c94-120">輸入</span><span class="sxs-lookup"><span data-stu-id="e3c94-120">INPUTS</span></span>

## <span data-ttu-id="e3c94-121">輸出</span><span class="sxs-lookup"><span data-stu-id="e3c94-121">OUTPUTS</span></span>

## <span data-ttu-id="e3c94-122">筆記</span><span class="sxs-lookup"><span data-stu-id="e3c94-122">NOTES</span></span>

## <span data-ttu-id="e3c94-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3c94-123">RELATED LINKS</span></span>

[<span data-ttu-id="e3c94-124">AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="e3c94-124">Get-AzureSiteRecoveryVaultSettings</span></span>](./Get-AzureSiteRecoveryVaultSettings.md)

[<span data-ttu-id="e3c94-125">AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e3c94-125">Get-AzureSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureSiteRecoveryVaultSettingsFile.md)


