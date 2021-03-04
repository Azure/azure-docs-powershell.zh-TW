---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 9d3a17280f80ef0376912f806439698f24cdfe25
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916451"
---
# <span data-ttu-id="5a520-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="5a520-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="5a520-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5a520-102">SYNOPSIS</span></span>

## <span data-ttu-id="5a520-103">語法</span><span class="sxs-lookup"><span data-stu-id="5a520-103">SYNTAX</span></span>

### <span data-ttu-id="5a520-104">S1</span><span class="sxs-lookup"><span data-stu-id="5a520-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a520-105">S2</span><span class="sxs-lookup"><span data-stu-id="5a520-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a520-106">描述</span><span class="sxs-lookup"><span data-stu-id="5a520-106">DESCRIPTION</span></span>
<span data-ttu-id="5a520-107">**Reset-AzWebAppPublishingProfile** Cmdlet 會重設指定 Web App 的發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="5a520-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="5a520-108">例子</span><span class="sxs-lookup"><span data-stu-id="5a520-108">EXAMPLES</span></span>

### <span data-ttu-id="5a520-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="5a520-109">Example 1</span></span>

<span data-ttu-id="5a520-110">下列範例會重設與資源群組 MyResourceGroup 相關聯的 Web App IpRule 發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="5a520-110">The following example resets the publishing profile for the Web App IpRule associated with the resource group MyResourceGroup.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Reset-AzWebAppPublishingProfile -Name IpRule -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="5a520-111">參數</span><span class="sxs-lookup"><span data-stu-id="5a520-111">PARAMETERS</span></span>

### <span data-ttu-id="5a520-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a520-112">-DefaultProfile</span></span>
<span data-ttu-id="5a520-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a520-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a520-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="5a520-114">-Name</span></span>
<span data-ttu-id="5a520-115">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="5a520-115">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a520-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a520-116">-ResourceGroupName</span></span>
<span data-ttu-id="5a520-117">資源組名</span><span class="sxs-lookup"><span data-stu-id="5a520-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a520-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5a520-118">-WebApp</span></span>
<span data-ttu-id="5a520-119">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="5a520-119">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a520-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a520-120">CommonParameters</span></span>
<span data-ttu-id="5a520-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5a520-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a520-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5a520-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a520-123">輸入</span><span class="sxs-lookup"><span data-stu-id="5a520-123">INPUTS</span></span>

### <span data-ttu-id="5a520-124">System.String</span><span class="sxs-lookup"><span data-stu-id="5a520-124">System.String</span></span>

### <span data-ttu-id="5a520-125">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="5a520-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5a520-126">輸出</span><span class="sxs-lookup"><span data-stu-id="5a520-126">OUTPUTS</span></span>

### <span data-ttu-id="5a520-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5a520-127">System.String</span></span>

## <span data-ttu-id="5a520-128">筆記</span><span class="sxs-lookup"><span data-stu-id="5a520-128">NOTES</span></span>

## <span data-ttu-id="5a520-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a520-129">RELATED LINKS</span></span>
