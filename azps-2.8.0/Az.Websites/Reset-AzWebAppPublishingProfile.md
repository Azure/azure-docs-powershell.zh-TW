---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 81eaa3b287a14cdc9aa71150c2f0b3724aeb4f4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792958"
---
# <span data-ttu-id="c53ae-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="c53ae-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="c53ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c53ae-102">SYNOPSIS</span></span>

## <span data-ttu-id="c53ae-103">句法</span><span class="sxs-lookup"><span data-stu-id="c53ae-103">SYNTAX</span></span>

### <span data-ttu-id="c53ae-104">S1</span><span class="sxs-lookup"><span data-stu-id="c53ae-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c53ae-105">S2</span><span class="sxs-lookup"><span data-stu-id="c53ae-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c53ae-106">說明</span><span class="sxs-lookup"><span data-stu-id="c53ae-106">DESCRIPTION</span></span>
<span data-ttu-id="c53ae-107">**Reset AzWebAppPublishingProfile** Cmdlet 會重設指定 Web App 的發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="c53ae-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="c53ae-108">示例</span><span class="sxs-lookup"><span data-stu-id="c53ae-108">EXAMPLES</span></span>

### <span data-ttu-id="c53ae-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="c53ae-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="c53ae-110">這個命令會針對與資源群組 Default Web-WestUS 相關聯的 Web App ContosoWebApp，重設其發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="c53ae-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c53ae-111">參數</span><span class="sxs-lookup"><span data-stu-id="c53ae-111">PARAMETERS</span></span>

### <span data-ttu-id="c53ae-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c53ae-112">-DefaultProfile</span></span>
<span data-ttu-id="c53ae-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c53ae-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c53ae-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="c53ae-114">-Name</span></span>
<span data-ttu-id="c53ae-115">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="c53ae-115">WebApp Name</span></span>

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

### <span data-ttu-id="c53ae-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c53ae-116">-ResourceGroupName</span></span>
<span data-ttu-id="c53ae-117">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c53ae-117">Resource Group Name</span></span>

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

### <span data-ttu-id="c53ae-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c53ae-118">-WebApp</span></span>
<span data-ttu-id="c53ae-119">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="c53ae-119">WebApp Object</span></span>

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

### <span data-ttu-id="c53ae-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c53ae-120">CommonParameters</span></span>
<span data-ttu-id="c53ae-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c53ae-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c53ae-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c53ae-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c53ae-123">輸入</span><span class="sxs-lookup"><span data-stu-id="c53ae-123">INPUTS</span></span>

### <span data-ttu-id="c53ae-124">System.object</span><span class="sxs-lookup"><span data-stu-id="c53ae-124">System.String</span></span>

### <span data-ttu-id="c53ae-125">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="c53ae-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c53ae-126">輸出</span><span class="sxs-lookup"><span data-stu-id="c53ae-126">OUTPUTS</span></span>

### <span data-ttu-id="c53ae-127">System.object</span><span class="sxs-lookup"><span data-stu-id="c53ae-127">System.String</span></span>

## <span data-ttu-id="c53ae-128">筆記</span><span class="sxs-lookup"><span data-stu-id="c53ae-128">NOTES</span></span>

## <span data-ttu-id="c53ae-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="c53ae-129">RELATED LINKS</span></span>
