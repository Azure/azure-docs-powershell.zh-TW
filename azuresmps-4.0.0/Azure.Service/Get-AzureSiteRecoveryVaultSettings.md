---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 305511DC-477F-4A33-8B16-063B39B19ED3
online version: ''
schema: 2.0.0
ms.openlocfilehash: cd96d7dd63791c5ef2e4a8a036949823d5c73313
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93968012"
---
# <span data-ttu-id="96ed5-101">Get-AzureSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="96ed5-101">Get-AzureSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="96ed5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96ed5-102">SYNOPSIS</span></span>
<span data-ttu-id="96ed5-103">取得網站恢復電子倉庫的設定。</span><span class="sxs-lookup"><span data-stu-id="96ed5-103">Gets settings for a Site Recovery vault.</span></span>

## <span data-ttu-id="96ed5-104">句法</span><span class="sxs-lookup"><span data-stu-id="96ed5-104">SYNTAX</span></span>

```
Get-AzureSiteRecoveryVaultSettings [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="96ed5-105">說明</span><span class="sxs-lookup"><span data-stu-id="96ed5-105">DESCRIPTION</span></span>
<span data-ttu-id="96ed5-106">**AzureSiteRecoveryVaultSettings** Cmdlet 會取得與目前 Azure Site Recovery 保存庫相關的設定。</span><span class="sxs-lookup"><span data-stu-id="96ed5-106">The **Get-AzureSiteRecoveryVaultSettings** cmdlet gets settings related to the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="96ed5-107">示例</span><span class="sxs-lookup"><span data-stu-id="96ed5-107">EXAMPLES</span></span>

### <span data-ttu-id="96ed5-108">範例1：取得設定資訊</span><span class="sxs-lookup"><span data-stu-id="96ed5-108">Example 1: Get settings information</span></span>
```
PS C:\> Get-AzureSiteRecoveryVaultSettings
ResourceName                                                CloudServiceName
------------                                                ----------------
ContosoVault                                                RecoveryServices-6JP23WE3SKKOM5AFQG2YQAI22MNOWK52QDKWMUP...
```

<span data-ttu-id="96ed5-109">這個命令會取得目前 Azure Site Recovery 保存庫的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="96ed5-109">This command gets settings information for the current  Azure Site Recovery vault.</span></span>

## <span data-ttu-id="96ed5-110">參數</span><span class="sxs-lookup"><span data-stu-id="96ed5-110">PARAMETERS</span></span>

### <span data-ttu-id="96ed5-111">-設定檔</span><span class="sxs-lookup"><span data-stu-id="96ed5-111">-Profile</span></span>
<span data-ttu-id="96ed5-112">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="96ed5-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="96ed5-113">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="96ed5-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="96ed5-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96ed5-114">CommonParameters</span></span>
<span data-ttu-id="96ed5-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96ed5-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96ed5-116">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="96ed5-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96ed5-117">輸入</span><span class="sxs-lookup"><span data-stu-id="96ed5-117">INPUTS</span></span>

## <span data-ttu-id="96ed5-118">輸出</span><span class="sxs-lookup"><span data-stu-id="96ed5-118">OUTPUTS</span></span>

## <span data-ttu-id="96ed5-119">筆記</span><span class="sxs-lookup"><span data-stu-id="96ed5-119">NOTES</span></span>

## <span data-ttu-id="96ed5-120">相關連結</span><span class="sxs-lookup"><span data-stu-id="96ed5-120">RELATED LINKS</span></span>

[<span data-ttu-id="96ed5-121">AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="96ed5-121">Get-AzureSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureSiteRecoveryVaultSettingsFile.md)

[<span data-ttu-id="96ed5-122">匯入-AzureSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="96ed5-122">Import-AzureSiteRecoveryVaultSettingsFile</span></span>](./Import-AzureSiteRecoveryVaultSettingsFile.md)


