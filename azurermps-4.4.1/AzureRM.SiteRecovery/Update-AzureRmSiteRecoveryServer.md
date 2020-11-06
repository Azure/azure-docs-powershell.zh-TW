---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: AD76C752-2070-449D-BF4F-B4260B05AB02
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 6afb5be21f1000cf2e18cd8a4b9e1dfa4f159ee0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452323"
---
# <span data-ttu-id="b82ce-101">Update-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="b82ce-101">Update-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="b82ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b82ce-102">SYNOPSIS</span></span>
<span data-ttu-id="b82ce-103">刷新網站恢復伺服器。</span><span class="sxs-lookup"><span data-stu-id="b82ce-103">Refreshes a Site Recovery server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b82ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="b82ce-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServer -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b82ce-105">說明</span><span class="sxs-lookup"><span data-stu-id="b82ce-105">DESCRIPTION</span></span>
<span data-ttu-id="b82ce-106">**AzureRmSiteRecoveryServer** Cmdlet 會重新整理 Azure Site Recovery 伺服器。</span><span class="sxs-lookup"><span data-stu-id="b82ce-106">The **Update-AzureRmSiteRecoveryServer** cmdlet refreshes an Azure Site Recovery server.</span></span>

## <span data-ttu-id="b82ce-107">示例</span><span class="sxs-lookup"><span data-stu-id="b82ce-107">EXAMPLES</span></span>

## <span data-ttu-id="b82ce-108">參數</span><span class="sxs-lookup"><span data-stu-id="b82ce-108">PARAMETERS</span></span>

### <span data-ttu-id="b82ce-109">-伺服器</span><span class="sxs-lookup"><span data-stu-id="b82ce-109">-Server</span></span>
<span data-ttu-id="b82ce-110">指定此 Cmdlet 更新的網站恢復伺服器。</span><span class="sxs-lookup"><span data-stu-id="b82ce-110">Specifies the Site Recovery server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b82ce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b82ce-111">-DefaultProfile</span></span>
<span data-ttu-id="b82ce-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b82ce-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b82ce-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b82ce-113">CommonParameters</span></span>
<span data-ttu-id="b82ce-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b82ce-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b82ce-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b82ce-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b82ce-116">輸入</span><span class="sxs-lookup"><span data-stu-id="b82ce-116">INPUTS</span></span>

### <span data-ttu-id="b82ce-117">ASRServer</span><span class="sxs-lookup"><span data-stu-id="b82ce-117">ASRServer</span></span>
<span data-ttu-id="b82ce-118">形參 "Server" 接受管線中 "ASRServer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="b82ce-118">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="b82ce-119">輸出</span><span class="sxs-lookup"><span data-stu-id="b82ce-119">OUTPUTS</span></span>

## <span data-ttu-id="b82ce-120">筆記</span><span class="sxs-lookup"><span data-stu-id="b82ce-120">NOTES</span></span>

## <span data-ttu-id="b82ce-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="b82ce-121">RELATED LINKS</span></span>

[<span data-ttu-id="b82ce-122">AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="b82ce-122">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="b82ce-123">移除-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="b82ce-123">Remove-AzureRmSiteRecoveryServer</span></span>](./Remove-AzureRmSiteRecoveryServer.md)
