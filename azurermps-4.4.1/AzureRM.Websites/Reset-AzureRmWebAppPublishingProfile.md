---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: f1224ae7ad95598d8ae947d0e38ef3a9cf7a4dba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447113"
---
# <span data-ttu-id="52798-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="52798-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="52798-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52798-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52798-103">句法</span><span class="sxs-lookup"><span data-stu-id="52798-103">SYNTAX</span></span>

### <span data-ttu-id="52798-104">S1</span><span class="sxs-lookup"><span data-stu-id="52798-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52798-105">S2</span><span class="sxs-lookup"><span data-stu-id="52798-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52798-106">說明</span><span class="sxs-lookup"><span data-stu-id="52798-106">DESCRIPTION</span></span>
<span data-ttu-id="52798-107">**Reset AzureRmWebAppPublishingProfile** Cmdlet 會重設指定 Web App 的發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="52798-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="52798-108">示例</span><span class="sxs-lookup"><span data-stu-id="52798-108">EXAMPLES</span></span>

### <span data-ttu-id="52798-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="52798-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="52798-110">這個命令會針對與資源群組 Default Web-WestUS 相關聯的 Web App ContosoWebApp，重設其發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="52798-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="52798-111">參數</span><span class="sxs-lookup"><span data-stu-id="52798-111">PARAMETERS</span></span>

### <span data-ttu-id="52798-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="52798-112">-Name</span></span>
<span data-ttu-id="52798-113">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="52798-113">WebApp Name</span></span>

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

### <span data-ttu-id="52798-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52798-114">-ResourceGroupName</span></span>
<span data-ttu-id="52798-115">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="52798-115">Resource Group Name</span></span>

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

### <span data-ttu-id="52798-116">-WebApp</span><span class="sxs-lookup"><span data-stu-id="52798-116">-WebApp</span></span>
<span data-ttu-id="52798-117">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="52798-117">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52798-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52798-118">-DefaultProfile</span></span>
<span data-ttu-id="52798-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="52798-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52798-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52798-120">CommonParameters</span></span>
<span data-ttu-id="52798-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52798-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52798-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="52798-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52798-123">輸入</span><span class="sxs-lookup"><span data-stu-id="52798-123">INPUTS</span></span>

### <span data-ttu-id="52798-124">網站地圖</span><span class="sxs-lookup"><span data-stu-id="52798-124">Site</span></span>
<span data-ttu-id="52798-125">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="52798-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="52798-126">輸出</span><span class="sxs-lookup"><span data-stu-id="52798-126">OUTPUTS</span></span>

## <span data-ttu-id="52798-127">筆記</span><span class="sxs-lookup"><span data-stu-id="52798-127">NOTES</span></span>

## <span data-ttu-id="52798-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="52798-128">RELATED LINKS</span></span>

