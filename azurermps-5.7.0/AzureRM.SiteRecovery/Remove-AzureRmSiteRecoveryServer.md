---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3302054E-C5BB-4B89-B9C9-ED7572DFA234
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServer.md
ms.openlocfilehash: 7c7afc0a1b6544f165f379a7363960142f73780d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625406"
---
# <span data-ttu-id="ca578-101">Remove-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="ca578-101">Remove-AzureRmSiteRecoveryServer</span></span>

## <span data-ttu-id="ca578-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca578-102">SYNOPSIS</span></span>
<span data-ttu-id="ca578-103">從目前的電子倉庫中移除網站復原伺服器。</span><span class="sxs-lookup"><span data-stu-id="ca578-103">Removes a Site Recovery server from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca578-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca578-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServer -Server <ASRServer> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca578-105">說明</span><span class="sxs-lookup"><span data-stu-id="ca578-105">DESCRIPTION</span></span>
<span data-ttu-id="ca578-106">**AzureRmSiteRecoveryServer** Cmdlet 會登出 Azure Site Recovery 伺服器，這會將它從目前的電子倉庫中移除。</span><span class="sxs-lookup"><span data-stu-id="ca578-106">The **Remove-AzureRmSiteRecoveryServer** cmdlet unregisters an Azure Site Recovery server which removes it from the current vault.</span></span>

## <span data-ttu-id="ca578-107">示例</span><span class="sxs-lookup"><span data-stu-id="ca578-107">EXAMPLES</span></span>

## <span data-ttu-id="ca578-108">參數</span><span class="sxs-lookup"><span data-stu-id="ca578-108">PARAMETERS</span></span>

### <span data-ttu-id="ca578-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca578-109">-DefaultProfile</span></span>
<span data-ttu-id="ca578-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca578-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca578-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ca578-111">-Force</span></span>
<span data-ttu-id="ca578-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ca578-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca578-113">-伺服器</span><span class="sxs-lookup"><span data-stu-id="ca578-113">-Server</span></span>
<span data-ttu-id="ca578-114">指定網站恢復伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="ca578-114">Specifies the Site Recovery server object.</span></span>

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca578-115">-確認</span><span class="sxs-lookup"><span data-stu-id="ca578-115">-Confirm</span></span>
<span data-ttu-id="ca578-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ca578-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca578-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca578-117">-WhatIf</span></span>
<span data-ttu-id="ca578-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca578-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ca578-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca578-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca578-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca578-120">CommonParameters</span></span>
<span data-ttu-id="ca578-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca578-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca578-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ca578-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca578-123">輸入</span><span class="sxs-lookup"><span data-stu-id="ca578-123">INPUTS</span></span>

### <span data-ttu-id="ca578-124">ASRServer</span><span class="sxs-lookup"><span data-stu-id="ca578-124">ASRServer</span></span>
<span data-ttu-id="ca578-125">形參 "Server" 接受管線中 "ASRServer" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ca578-125">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="ca578-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ca578-126">OUTPUTS</span></span>

### <span data-ttu-id="ca578-127">System.object. IEnumerable ' 1 [SiteRecovery. ASRServer] （）</span><span class="sxs-lookup"><span data-stu-id="ca578-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRServer]</span></span>

## <span data-ttu-id="ca578-128">筆記</span><span class="sxs-lookup"><span data-stu-id="ca578-128">NOTES</span></span>

## <span data-ttu-id="ca578-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca578-129">RELATED LINKS</span></span>

[<span data-ttu-id="ca578-130">AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="ca578-130">Get-AzureRmSiteRecoveryServer</span></span>](./Get-AzureRmSiteRecoveryServer.md)

[<span data-ttu-id="ca578-131">更新-AzureRmSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="ca578-131">Update-AzureRmSiteRecoveryServer</span></span>](./Update-AzureRmSiteRecoveryServer.md)
