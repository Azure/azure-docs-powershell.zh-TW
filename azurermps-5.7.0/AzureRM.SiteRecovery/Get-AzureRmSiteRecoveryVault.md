---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7C15B0AA-D97E-4715-9AD4-971731527D09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: f3988d28633ba879ebf78c57e235f4f07d6deced
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625418"
---
# <span data-ttu-id="695db-101">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="695db-101">Get-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="695db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="695db-102">SYNOPSIS</span></span>
<span data-ttu-id="695db-103">從目前的訂閱取得網站復原保存庫。</span><span class="sxs-lookup"><span data-stu-id="695db-103">Gets Site Recovery vaults from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="695db-104">句法</span><span class="sxs-lookup"><span data-stu-id="695db-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="695db-105">說明</span><span class="sxs-lookup"><span data-stu-id="695db-105">DESCRIPTION</span></span>
<span data-ttu-id="695db-106">**AzureRmSiteRecoveryVault** Cmdlet 會從目前的訂閱取得 Azure Site recovery 保存庫或特定網站復原保存庫的清單。</span><span class="sxs-lookup"><span data-stu-id="695db-106">The **Get-AzureRmSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="695db-107">示例</span><span class="sxs-lookup"><span data-stu-id="695db-107">EXAMPLES</span></span>

## <span data-ttu-id="695db-108">參數</span><span class="sxs-lookup"><span data-stu-id="695db-108">PARAMETERS</span></span>

### <span data-ttu-id="695db-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="695db-109">-DefaultProfile</span></span>
<span data-ttu-id="695db-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="695db-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="695db-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="695db-111">-Name</span></span>
<span data-ttu-id="695db-112">指定保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="695db-112">Specifies the name of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695db-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="695db-113">-ResourceGroupName</span></span>
<span data-ttu-id="695db-114">指定要取得恢復服務物件的 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="695db-114">Specifies the name of the Azure resource group from which to get the recovery services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="695db-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="695db-115">CommonParameters</span></span>
<span data-ttu-id="695db-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="695db-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="695db-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="695db-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="695db-118">輸入</span><span class="sxs-lookup"><span data-stu-id="695db-118">INPUTS</span></span>

### <span data-ttu-id="695db-119">所有</span><span class="sxs-lookup"><span data-stu-id="695db-119">None</span></span>
<span data-ttu-id="695db-120">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="695db-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="695db-121">輸出</span><span class="sxs-lookup"><span data-stu-id="695db-121">OUTPUTS</span></span>

### <span data-ttu-id="695db-122">[System.object]. 清單 ' 1 [SiteRecovery. ASRVault]</span><span class="sxs-lookup"><span data-stu-id="695db-122">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVault]</span></span>

## <span data-ttu-id="695db-123">筆記</span><span class="sxs-lookup"><span data-stu-id="695db-123">NOTES</span></span>

## <span data-ttu-id="695db-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="695db-124">RELATED LINKS</span></span>

[<span data-ttu-id="695db-125">新-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="695db-125">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="695db-126">移除-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="695db-126">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
