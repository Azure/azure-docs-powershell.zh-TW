---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: DE1D5A0D-2545-4F01-98B5-684ED0D25230
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
ms.openlocfilehash: f052b11a11fa77047d424b7045b127a75043cc25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624762"
---
# <span data-ttu-id="2c59f-101">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="2c59f-101">Remove-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="2c59f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c59f-102">SYNOPSIS</span></span>
<span data-ttu-id="2c59f-103">從目前的電子倉庫中移除網站恢復網站。</span><span class="sxs-lookup"><span data-stu-id="2c59f-103">Removes a Site Recovery site from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c59f-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c59f-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoverySite -Site <ASRSite> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c59f-105">說明</span><span class="sxs-lookup"><span data-stu-id="2c59f-105">DESCRIPTION</span></span>
<span data-ttu-id="2c59f-106">**AzureRmSiteRecoverySite** Cmdlet 會從目前的保存庫刪除 Azure Site Recovery 網站。</span><span class="sxs-lookup"><span data-stu-id="2c59f-106">The **Remove-AzureRmSiteRecoverySite** cmdlet deletes an Azure Site Recovery site from the current vault.</span></span>

## <span data-ttu-id="2c59f-107">示例</span><span class="sxs-lookup"><span data-stu-id="2c59f-107">EXAMPLES</span></span>

## <span data-ttu-id="2c59f-108">參數</span><span class="sxs-lookup"><span data-stu-id="2c59f-108">PARAMETERS</span></span>

### <span data-ttu-id="2c59f-109">-Force</span><span class="sxs-lookup"><span data-stu-id="2c59f-109">-Force</span></span>
<span data-ttu-id="2c59f-110">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2c59f-110">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c59f-111">-網站</span><span class="sxs-lookup"><span data-stu-id="2c59f-111">-Site</span></span>
<span data-ttu-id="2c59f-112">指定網站復原網站物件。</span><span class="sxs-lookup"><span data-stu-id="2c59f-112">Specifies the Site Recovery site object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRSite
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c59f-113">-確認</span><span class="sxs-lookup"><span data-stu-id="2c59f-113">-Confirm</span></span>
<span data-ttu-id="2c59f-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2c59f-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c59f-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c59f-115">-WhatIf</span></span>
<span data-ttu-id="2c59f-116">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2c59f-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2c59f-117">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2c59f-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c59f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c59f-118">-DefaultProfile</span></span>
<span data-ttu-id="2c59f-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c59f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c59f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c59f-120">CommonParameters</span></span>
<span data-ttu-id="2c59f-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2c59f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c59f-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2c59f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c59f-123">輸入</span><span class="sxs-lookup"><span data-stu-id="2c59f-123">INPUTS</span></span>

### <span data-ttu-id="2c59f-124">ASRSite</span><span class="sxs-lookup"><span data-stu-id="2c59f-124">ASRSite</span></span>
<span data-ttu-id="2c59f-125">參數 "Site" 接受管道中類型 ' ASRSite」的值</span><span class="sxs-lookup"><span data-stu-id="2c59f-125">Parameter 'Site' accepts value of type 'ASRSite' from the pipeline</span></span>

## <span data-ttu-id="2c59f-126">輸出</span><span class="sxs-lookup"><span data-stu-id="2c59f-126">OUTPUTS</span></span>

## <span data-ttu-id="2c59f-127">筆記</span><span class="sxs-lookup"><span data-stu-id="2c59f-127">NOTES</span></span>

## <span data-ttu-id="2c59f-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c59f-128">RELATED LINKS</span></span>

[<span data-ttu-id="2c59f-129">AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="2c59f-129">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="2c59f-130">新-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="2c59f-130">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)
