---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: 455a1735df128ee84d99adb6461c602a7b1dbbdf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614226"
---
# <span data-ttu-id="fa4a8-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fa4a8-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="fa4a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fa4a8-102">SYNOPSIS</span></span>
<span data-ttu-id="fa4a8-103">停止 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="fa4a8-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="fa4a8-104">句法</span><span class="sxs-lookup"><span data-stu-id="fa4a8-104">SYNTAX</span></span>

### <span data-ttu-id="fa4a8-105">S1</span><span class="sxs-lookup"><span data-stu-id="fa4a8-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa4a8-106">S2</span><span class="sxs-lookup"><span data-stu-id="fa4a8-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa4a8-107">說明</span><span class="sxs-lookup"><span data-stu-id="fa4a8-107">DESCRIPTION</span></span>
<span data-ttu-id="fa4a8-108">**AzWebAppSlot** Cmdlet 會停止 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="fa4a8-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="fa4a8-109">示例</span><span class="sxs-lookup"><span data-stu-id="fa4a8-109">EXAMPLES</span></span>

### <span data-ttu-id="fa4a8-110">範例1</span><span class="sxs-lookup"><span data-stu-id="fa4a8-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="fa4a8-111">這個命令會停止與屬於名為「預設-Web-WestUS」之資源群組的名為 ContosoWebApp 的 Web App 相關的槽 Slot001。</span><span class="sxs-lookup"><span data-stu-id="fa4a8-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="fa4a8-112">參數</span><span class="sxs-lookup"><span data-stu-id="fa4a8-112">PARAMETERS</span></span>

### <span data-ttu-id="fa4a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa4a8-113">-DefaultProfile</span></span>
<span data-ttu-id="fa4a8-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fa4a8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa4a8-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="fa4a8-115">-Name</span></span>
<span data-ttu-id="fa4a8-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="fa4a8-116">WebApp Name</span></span>

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

### <span data-ttu-id="fa4a8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa4a8-117">-ResourceGroupName</span></span>
<span data-ttu-id="fa4a8-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="fa4a8-118">Resource Group Name</span></span>

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

### <span data-ttu-id="fa4a8-119">-槽</span><span class="sxs-lookup"><span data-stu-id="fa4a8-119">-Slot</span></span>
<span data-ttu-id="fa4a8-120">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="fa4a8-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="fa4a8-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fa4a8-121">-WebApp</span></span>
<span data-ttu-id="fa4a8-122">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="fa4a8-122">WebApp Object</span></span>

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

### <span data-ttu-id="fa4a8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa4a8-123">CommonParameters</span></span>
<span data-ttu-id="fa4a8-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fa4a8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa4a8-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fa4a8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa4a8-126">輸入</span><span class="sxs-lookup"><span data-stu-id="fa4a8-126">INPUTS</span></span>

### <span data-ttu-id="fa4a8-127">System.object</span><span class="sxs-lookup"><span data-stu-id="fa4a8-127">System.String</span></span>

### <span data-ttu-id="fa4a8-128">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="fa4a8-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="fa4a8-129">輸出</span><span class="sxs-lookup"><span data-stu-id="fa4a8-129">OUTPUTS</span></span>

### <span data-ttu-id="fa4a8-130">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="fa4a8-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="fa4a8-131">筆記</span><span class="sxs-lookup"><span data-stu-id="fa4a8-131">NOTES</span></span>

## <span data-ttu-id="fa4a8-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa4a8-132">RELATED LINKS</span></span>
