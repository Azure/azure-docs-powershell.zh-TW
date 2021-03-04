---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: bdee1c1fdda561d7265b3f6ff52a443238b6d2b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913285"
---
# <span data-ttu-id="e2390-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="e2390-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="e2390-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e2390-102">SYNOPSIS</span></span>

## <span data-ttu-id="e2390-103">語法</span><span class="sxs-lookup"><span data-stu-id="e2390-103">SYNTAX</span></span>

### <span data-ttu-id="e2390-104">S1</span><span class="sxs-lookup"><span data-stu-id="e2390-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2390-105">S2</span><span class="sxs-lookup"><span data-stu-id="e2390-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2390-106">描述</span><span class="sxs-lookup"><span data-stu-id="e2390-106">DESCRIPTION</span></span>
<span data-ttu-id="e2390-107">**Reset-AzWebAppSlotPublishingProfile** Cmdlet 會重設指定 Web App Slot 的發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="e2390-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="e2390-108">例子</span><span class="sxs-lookup"><span data-stu-id="e2390-108">EXAMPLES</span></span>

### <span data-ttu-id="e2390-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="e2390-109">Example 1</span></span>
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="e2390-110">此命令會重設與資源群組 Default-Web-WestUS 相關聯的 Web App ContosoWebApp Slot 名稱 slot 的發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="e2390-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="e2390-111">參數</span><span class="sxs-lookup"><span data-stu-id="e2390-111">PARAMETERS</span></span>

### <span data-ttu-id="e2390-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2390-112">-DefaultProfile</span></span>
<span data-ttu-id="e2390-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e2390-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2390-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="e2390-114">-Name</span></span>
<span data-ttu-id="e2390-115">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="e2390-115">WebApp Name</span></span>

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

### <span data-ttu-id="e2390-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2390-116">-ResourceGroupName</span></span>
<span data-ttu-id="e2390-117">資源組名</span><span class="sxs-lookup"><span data-stu-id="e2390-117">Resource Group Name</span></span>

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

### <span data-ttu-id="e2390-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="e2390-118">-Slot</span></span>
<span data-ttu-id="e2390-119">WebApp Slot 名稱</span><span class="sxs-lookup"><span data-stu-id="e2390-119">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2390-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e2390-120">-WebApp</span></span>
<span data-ttu-id="e2390-121">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="e2390-121">WebApp Object</span></span>

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

### <span data-ttu-id="e2390-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2390-122">CommonParameters</span></span>
<span data-ttu-id="e2390-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e2390-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2390-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e2390-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2390-125">輸入</span><span class="sxs-lookup"><span data-stu-id="e2390-125">INPUTS</span></span>

### <span data-ttu-id="e2390-126">System.String</span><span class="sxs-lookup"><span data-stu-id="e2390-126">System.String</span></span>

### <span data-ttu-id="e2390-127">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="e2390-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e2390-128">輸出</span><span class="sxs-lookup"><span data-stu-id="e2390-128">OUTPUTS</span></span>

### <span data-ttu-id="e2390-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e2390-129">System.String</span></span>

## <span data-ttu-id="e2390-130">筆記</span><span class="sxs-lookup"><span data-stu-id="e2390-130">NOTES</span></span>

## <span data-ttu-id="e2390-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2390-131">RELATED LINKS</span></span>
