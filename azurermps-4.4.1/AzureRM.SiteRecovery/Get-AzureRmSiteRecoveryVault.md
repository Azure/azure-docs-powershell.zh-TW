---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7C15B0AA-D97E-4715-9AD4-971731527D09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 37e0096dd6f279c13909f1b542e603faebfd1e97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625062"
---
# <span data-ttu-id="79155-101">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="79155-101">Get-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="79155-102">摘要</span><span class="sxs-lookup"><span data-stu-id="79155-102">SYNOPSIS</span></span>
<span data-ttu-id="79155-103">從目前的訂閱取得網站復原保存庫。</span><span class="sxs-lookup"><span data-stu-id="79155-103">Gets Site Recovery vaults from the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79155-104">句法</span><span class="sxs-lookup"><span data-stu-id="79155-104">SYNTAX</span></span>

```
Get-AzureRmSiteRecoveryVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79155-105">說明</span><span class="sxs-lookup"><span data-stu-id="79155-105">DESCRIPTION</span></span>
<span data-ttu-id="79155-106">**AzureRmSiteRecoveryVault** Cmdlet 會從目前的訂閱取得 Azure Site recovery 保存庫或特定網站復原保存庫的清單。</span><span class="sxs-lookup"><span data-stu-id="79155-106">The **Get-AzureRmSiteRecoveryVault** cmdlet gets a list of Azure Site Recovery vaults or a specific Site Recovery vault from the current subscription.</span></span>

## <span data-ttu-id="79155-107">示例</span><span class="sxs-lookup"><span data-stu-id="79155-107">EXAMPLES</span></span>

## <span data-ttu-id="79155-108">參數</span><span class="sxs-lookup"><span data-stu-id="79155-108">PARAMETERS</span></span>

### <span data-ttu-id="79155-109">-名稱</span><span class="sxs-lookup"><span data-stu-id="79155-109">-Name</span></span>
<span data-ttu-id="79155-110">指定保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="79155-110">Specifies the name of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79155-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79155-111">-ResourceGroupName</span></span>
<span data-ttu-id="79155-112">指定要取得恢復服務物件的 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="79155-112">Specifies the name of the Azure resource group from which to get the recovery services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79155-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79155-113">-DefaultProfile</span></span>
<span data-ttu-id="79155-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="79155-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79155-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79155-115">CommonParameters</span></span>
<span data-ttu-id="79155-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="79155-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79155-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="79155-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79155-118">輸入</span><span class="sxs-lookup"><span data-stu-id="79155-118">INPUTS</span></span>

## <span data-ttu-id="79155-119">輸出</span><span class="sxs-lookup"><span data-stu-id="79155-119">OUTPUTS</span></span>

### <span data-ttu-id="79155-120">[System.object]. 清單 ' 1 [SiteRecovery. ASRVault]</span><span class="sxs-lookup"><span data-stu-id="79155-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRVault]</span></span>

## <span data-ttu-id="79155-121">筆記</span><span class="sxs-lookup"><span data-stu-id="79155-121">NOTES</span></span>

## <span data-ttu-id="79155-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="79155-122">RELATED LINKS</span></span>

[<span data-ttu-id="79155-123">新-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="79155-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="79155-124">移除-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="79155-124">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
