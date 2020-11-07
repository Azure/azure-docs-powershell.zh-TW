---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 7F6B72A5-12F5-47EA-B5C3-E22F73377D8F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 0b70fe2636ae0bc460afd05f9428708c0ff4963b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625409"
---
# <span data-ttu-id="5e308-101">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="5e308-101">New-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="5e308-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e308-102">SYNOPSIS</span></span>
<span data-ttu-id="5e308-103">建立網站復原服務電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="5e308-103">Creates a Site Recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e308-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e308-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e308-105">說明</span><span class="sxs-lookup"><span data-stu-id="5e308-105">DESCRIPTION</span></span>
<span data-ttu-id="5e308-106">**新的-AzureRmSiteRecoveryVault** Cmdlet 會建立 Azure Site Recovery 服務保存庫。</span><span class="sxs-lookup"><span data-stu-id="5e308-106">The **New-AzureRmSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="5e308-107">示例</span><span class="sxs-lookup"><span data-stu-id="5e308-107">EXAMPLES</span></span>

## <span data-ttu-id="5e308-108">參數</span><span class="sxs-lookup"><span data-stu-id="5e308-108">PARAMETERS</span></span>

### <span data-ttu-id="5e308-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e308-109">-DefaultProfile</span></span>
<span data-ttu-id="5e308-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e308-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e308-111">-位置</span><span class="sxs-lookup"><span data-stu-id="5e308-111">-Location</span></span>
<span data-ttu-id="5e308-112">指定地理位置名稱。</span><span class="sxs-lookup"><span data-stu-id="5e308-112">Specifies the geographical location name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e308-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e308-113">-Name</span></span>
<span data-ttu-id="5e308-114">指定保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e308-114">Specifies the name of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e308-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e308-115">-ResourceGroupName</span></span>
<span data-ttu-id="5e308-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e308-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e308-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e308-117">CommonParameters</span></span>
<span data-ttu-id="5e308-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e308-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e308-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5e308-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e308-120">輸入</span><span class="sxs-lookup"><span data-stu-id="5e308-120">INPUTS</span></span>

### <span data-ttu-id="5e308-121">所有</span><span class="sxs-lookup"><span data-stu-id="5e308-121">None</span></span>
<span data-ttu-id="5e308-122">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="5e308-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5e308-123">輸出</span><span class="sxs-lookup"><span data-stu-id="5e308-123">OUTPUTS</span></span>

## <span data-ttu-id="5e308-124">筆記</span><span class="sxs-lookup"><span data-stu-id="5e308-124">NOTES</span></span>

## <span data-ttu-id="5e308-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e308-125">RELATED LINKS</span></span>

[<span data-ttu-id="5e308-126">AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="5e308-126">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="5e308-127">移除-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="5e308-127">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
