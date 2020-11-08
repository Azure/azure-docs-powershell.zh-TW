---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 81005ceac6bfa3c258a147f3fbef168e95c302cb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140693"
---
# <span data-ttu-id="83341-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="83341-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="83341-102">摘要</span><span class="sxs-lookup"><span data-stu-id="83341-102">SYNOPSIS</span></span>

## <span data-ttu-id="83341-103">句法</span><span class="sxs-lookup"><span data-stu-id="83341-103">SYNTAX</span></span>

### <span data-ttu-id="83341-104">S1</span><span class="sxs-lookup"><span data-stu-id="83341-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83341-105">S2</span><span class="sxs-lookup"><span data-stu-id="83341-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83341-106">說明</span><span class="sxs-lookup"><span data-stu-id="83341-106">DESCRIPTION</span></span>
<span data-ttu-id="83341-107">**Reset AzWebAppPublishingProfile** Cmdlet 會重設指定 Web App 的發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="83341-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="83341-108">示例</span><span class="sxs-lookup"><span data-stu-id="83341-108">EXAMPLES</span></span>

### <span data-ttu-id="83341-109">範例1</span><span class="sxs-lookup"><span data-stu-id="83341-109">Example 1</span></span>

<span data-ttu-id="83341-110">下列範例會重設與資源群組 MyResourceGroup 相關聯之 Web App IpRule 的發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="83341-110">The following example resets the publishing profile for the Web App IpRule associated with the resource group MyResourceGroup.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Reset-AzWebAppPublishingProfile -Name IpRule -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="83341-111">參數</span><span class="sxs-lookup"><span data-stu-id="83341-111">PARAMETERS</span></span>

### <span data-ttu-id="83341-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83341-112">-DefaultProfile</span></span>
<span data-ttu-id="83341-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="83341-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83341-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="83341-114">-Name</span></span>
<span data-ttu-id="83341-115">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="83341-115">WebApp Name</span></span>

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

### <span data-ttu-id="83341-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83341-116">-ResourceGroupName</span></span>
<span data-ttu-id="83341-117">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="83341-117">Resource Group Name</span></span>

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

### <span data-ttu-id="83341-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="83341-118">-WebApp</span></span>
<span data-ttu-id="83341-119">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="83341-119">WebApp Object</span></span>

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

### <span data-ttu-id="83341-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83341-120">CommonParameters</span></span>
<span data-ttu-id="83341-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="83341-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83341-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="83341-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83341-123">輸入</span><span class="sxs-lookup"><span data-stu-id="83341-123">INPUTS</span></span>

### <span data-ttu-id="83341-124">System.object</span><span class="sxs-lookup"><span data-stu-id="83341-124">System.String</span></span>

### <span data-ttu-id="83341-125">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="83341-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="83341-126">輸出</span><span class="sxs-lookup"><span data-stu-id="83341-126">OUTPUTS</span></span>

### <span data-ttu-id="83341-127">System.object</span><span class="sxs-lookup"><span data-stu-id="83341-127">System.String</span></span>

## <span data-ttu-id="83341-128">筆記</span><span class="sxs-lookup"><span data-stu-id="83341-128">NOTES</span></span>

## <span data-ttu-id="83341-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="83341-129">RELATED LINKS</span></span>