---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 840e0bb2bfa10a89a5ba963e83ab434e795b3dd4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274083"
---
# <span data-ttu-id="a4c64-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="a4c64-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="a4c64-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a4c64-102">SYNOPSIS</span></span>

## <span data-ttu-id="a4c64-103">句法</span><span class="sxs-lookup"><span data-stu-id="a4c64-103">SYNTAX</span></span>

### <span data-ttu-id="a4c64-104">S1</span><span class="sxs-lookup"><span data-stu-id="a4c64-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4c64-105">S2</span><span class="sxs-lookup"><span data-stu-id="a4c64-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4c64-106">說明</span><span class="sxs-lookup"><span data-stu-id="a4c64-106">DESCRIPTION</span></span>
<span data-ttu-id="a4c64-107">**Reset AzWebAppSlotPublishingProfile** Cmdlet 會重設指定 Web App 槽的發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="a4c64-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="a4c64-108">示例</span><span class="sxs-lookup"><span data-stu-id="a4c64-108">EXAMPLES</span></span>

### <span data-ttu-id="a4c64-109">範例1</span><span class="sxs-lookup"><span data-stu-id="a4c64-109">Example 1</span></span>
```powershell
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="a4c64-110">這個命令會針對與資源群組 Default-Web-WestUS 相關聯的 Web App ContosoWebApp，重設 slot001 之槽的發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="a4c64-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a4c64-111">參數</span><span class="sxs-lookup"><span data-stu-id="a4c64-111">PARAMETERS</span></span>

### <span data-ttu-id="a4c64-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4c64-112">-DefaultProfile</span></span>
<span data-ttu-id="a4c64-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4c64-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4c64-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="a4c64-114">-Name</span></span>
<span data-ttu-id="a4c64-115">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="a4c64-115">WebApp Name</span></span>

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

### <span data-ttu-id="a4c64-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4c64-116">-ResourceGroupName</span></span>
<span data-ttu-id="a4c64-117">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="a4c64-117">Resource Group Name</span></span>

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

### <span data-ttu-id="a4c64-118">-槽</span><span class="sxs-lookup"><span data-stu-id="a4c64-118">-Slot</span></span>
<span data-ttu-id="a4c64-119">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="a4c64-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="a4c64-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a4c64-120">-WebApp</span></span>
<span data-ttu-id="a4c64-121">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="a4c64-121">WebApp Object</span></span>

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

### <span data-ttu-id="a4c64-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4c64-122">CommonParameters</span></span>
<span data-ttu-id="a4c64-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a4c64-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4c64-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a4c64-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4c64-125">輸入</span><span class="sxs-lookup"><span data-stu-id="a4c64-125">INPUTS</span></span>

### <span data-ttu-id="a4c64-126">System.object</span><span class="sxs-lookup"><span data-stu-id="a4c64-126">System.String</span></span>

### <span data-ttu-id="a4c64-127">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="a4c64-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a4c64-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a4c64-128">OUTPUTS</span></span>

### <span data-ttu-id="a4c64-129">System.object</span><span class="sxs-lookup"><span data-stu-id="a4c64-129">System.String</span></span>

## <span data-ttu-id="a4c64-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a4c64-130">NOTES</span></span>

## <span data-ttu-id="a4c64-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4c64-131">RELATED LINKS</span></span>
