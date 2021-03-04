---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 2157c7a570f38838a65e1d4bba40dade22e10367
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904565"
---
# <span data-ttu-id="ab280-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="ab280-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="ab280-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ab280-102">SYNOPSIS</span></span>
<span data-ttu-id="ab280-103">取得 Web App Slot Config 名稱清單</span><span class="sxs-lookup"><span data-stu-id="ab280-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="ab280-104">語法</span><span class="sxs-lookup"><span data-stu-id="ab280-104">SYNTAX</span></span>

### <span data-ttu-id="ab280-105">S1</span><span class="sxs-lookup"><span data-stu-id="ab280-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab280-106">S2</span><span class="sxs-lookup"><span data-stu-id="ab280-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab280-107">描述</span><span class="sxs-lookup"><span data-stu-id="ab280-107">DESCRIPTION</span></span>
<span data-ttu-id="ab280-108">**Get-AzWebAppSlotConfigName** Cmdlet 會取得目前標示為插槽設定的應用程式設定和連接字串名稱清單</span><span class="sxs-lookup"><span data-stu-id="ab280-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="ab280-109">例子</span><span class="sxs-lookup"><span data-stu-id="ab280-109">EXAMPLES</span></span>

### <span data-ttu-id="ab280-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="ab280-110">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="ab280-111">此命令會獲得與資源群組 Default-Web-WestUS 相關聯的名為 ContosoSite 之 Web App 的 App 設定和連接字串</span><span class="sxs-lookup"><span data-stu-id="ab280-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="ab280-112">參數</span><span class="sxs-lookup"><span data-stu-id="ab280-112">PARAMETERS</span></span>

### <span data-ttu-id="ab280-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab280-113">-DefaultProfile</span></span>
<span data-ttu-id="ab280-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab280-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab280-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab280-115">-Name</span></span>
<span data-ttu-id="ab280-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="ab280-116">WebApp Name</span></span>

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

### <span data-ttu-id="ab280-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab280-117">-ResourceGroupName</span></span>
<span data-ttu-id="ab280-118">資源組名</span><span class="sxs-lookup"><span data-stu-id="ab280-118">Resource Group Name</span></span>

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

### <span data-ttu-id="ab280-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ab280-119">-WebApp</span></span>
<span data-ttu-id="ab280-120">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="ab280-120">WebApp Object</span></span>

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

### <span data-ttu-id="ab280-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab280-121">CommonParameters</span></span>
<span data-ttu-id="ab280-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ab280-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab280-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ab280-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab280-124">輸入</span><span class="sxs-lookup"><span data-stu-id="ab280-124">INPUTS</span></span>

### <span data-ttu-id="ab280-125">System.String</span><span class="sxs-lookup"><span data-stu-id="ab280-125">System.String</span></span>

### <span data-ttu-id="ab280-126">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ab280-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ab280-127">輸出</span><span class="sxs-lookup"><span data-stu-id="ab280-127">OUTPUTS</span></span>

### <span data-ttu-id="ab280-128">Microsoft.Azure.management.Websites.models.SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="ab280-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="ab280-129">筆記</span><span class="sxs-lookup"><span data-stu-id="ab280-129">NOTES</span></span>

## <span data-ttu-id="ab280-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab280-130">RELATED LINKS</span></span>
