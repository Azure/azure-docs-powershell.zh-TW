---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/reset-Azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 519a072a0c51f489a78992e483dec8aa9cd1fab5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794959"
---
# <span data-ttu-id="2905f-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="2905f-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="2905f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2905f-102">SYNOPSIS</span></span>

## <span data-ttu-id="2905f-103">句法</span><span class="sxs-lookup"><span data-stu-id="2905f-103">SYNTAX</span></span>

### <span data-ttu-id="2905f-104">S1</span><span class="sxs-lookup"><span data-stu-id="2905f-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2905f-105">S2</span><span class="sxs-lookup"><span data-stu-id="2905f-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2905f-106">說明</span><span class="sxs-lookup"><span data-stu-id="2905f-106">DESCRIPTION</span></span>
<span data-ttu-id="2905f-107">**Reset AzWebAppPublishingProfile** Cmdlet 會重設指定 Web App 的發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="2905f-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="2905f-108">示例</span><span class="sxs-lookup"><span data-stu-id="2905f-108">EXAMPLES</span></span>

### <span data-ttu-id="2905f-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="2905f-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="2905f-110">這個命令會針對與資源群組 Default Web-WestUS 相關聯的 Web App ContosoWebApp，重設其發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="2905f-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="2905f-111">參數</span><span class="sxs-lookup"><span data-stu-id="2905f-111">PARAMETERS</span></span>

### <span data-ttu-id="2905f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2905f-112">-DefaultProfile</span></span>
<span data-ttu-id="2905f-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2905f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2905f-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="2905f-114">-Name</span></span>
<span data-ttu-id="2905f-115">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="2905f-115">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2905f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2905f-116">-ResourceGroupName</span></span>
<span data-ttu-id="2905f-117">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2905f-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2905f-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2905f-118">-WebApp</span></span>
<span data-ttu-id="2905f-119">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="2905f-119">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2905f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2905f-120">CommonParameters</span></span>
<span data-ttu-id="2905f-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2905f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2905f-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2905f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2905f-123">輸入</span><span class="sxs-lookup"><span data-stu-id="2905f-123">INPUTS</span></span>

### <span data-ttu-id="2905f-124">網站地圖</span><span class="sxs-lookup"><span data-stu-id="2905f-124">Site</span></span>
<span data-ttu-id="2905f-125">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="2905f-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2905f-126">輸出</span><span class="sxs-lookup"><span data-stu-id="2905f-126">OUTPUTS</span></span>

## <span data-ttu-id="2905f-127">筆記</span><span class="sxs-lookup"><span data-stu-id="2905f-127">NOTES</span></span>

## <span data-ttu-id="2905f-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="2905f-128">RELATED LINKS</span></span>

