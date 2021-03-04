---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/powershell/module/az.websites/stop-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: 1be0602fc139c5630591dea1e7aa35eaaf27a714
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916801"
---
# <span data-ttu-id="59e42-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="59e42-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="59e42-102">簡介</span><span class="sxs-lookup"><span data-stu-id="59e42-102">SYNOPSIS</span></span>
<span data-ttu-id="59e42-103">停止 Azure Web App 插槽。</span><span class="sxs-lookup"><span data-stu-id="59e42-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="59e42-104">語法</span><span class="sxs-lookup"><span data-stu-id="59e42-104">SYNTAX</span></span>

### <span data-ttu-id="59e42-105">S1</span><span class="sxs-lookup"><span data-stu-id="59e42-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59e42-106">S2</span><span class="sxs-lookup"><span data-stu-id="59e42-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59e42-107">描述</span><span class="sxs-lookup"><span data-stu-id="59e42-107">DESCRIPTION</span></span>
<span data-ttu-id="59e42-108">**Stop-AzWebAppSlot** Cmdlet 會停止 Azure Web App Slot。</span><span class="sxs-lookup"><span data-stu-id="59e42-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="59e42-109">例子</span><span class="sxs-lookup"><span data-stu-id="59e42-109">EXAMPLES</span></span>

### <span data-ttu-id="59e42-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="59e42-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="59e42-111">此命令會停止與名為 ContosoWebApp 的 Web App 相關的插槽 Slot Slot001，該 Web App 屬於 Default-Web-WestUS 資源群組。</span><span class="sxs-lookup"><span data-stu-id="59e42-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="59e42-112">參數</span><span class="sxs-lookup"><span data-stu-id="59e42-112">PARAMETERS</span></span>

### <span data-ttu-id="59e42-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59e42-113">-DefaultProfile</span></span>
<span data-ttu-id="59e42-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="59e42-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59e42-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="59e42-115">-Name</span></span>
<span data-ttu-id="59e42-116">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="59e42-116">WebApp Name</span></span>

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

### <span data-ttu-id="59e42-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59e42-117">-ResourceGroupName</span></span>
<span data-ttu-id="59e42-118">資源組名</span><span class="sxs-lookup"><span data-stu-id="59e42-118">Resource Group Name</span></span>

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

### <span data-ttu-id="59e42-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="59e42-119">-Slot</span></span>
<span data-ttu-id="59e42-120">WebApp Slot 名稱</span><span class="sxs-lookup"><span data-stu-id="59e42-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="59e42-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="59e42-121">-WebApp</span></span>
<span data-ttu-id="59e42-122">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="59e42-122">WebApp Object</span></span>

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

### <span data-ttu-id="59e42-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59e42-123">CommonParameters</span></span>
<span data-ttu-id="59e42-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="59e42-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59e42-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="59e42-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59e42-126">輸入</span><span class="sxs-lookup"><span data-stu-id="59e42-126">INPUTS</span></span>

### <span data-ttu-id="59e42-127">System.String</span><span class="sxs-lookup"><span data-stu-id="59e42-127">System.String</span></span>

### <span data-ttu-id="59e42-128">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="59e42-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="59e42-129">輸出</span><span class="sxs-lookup"><span data-stu-id="59e42-129">OUTPUTS</span></span>

### <span data-ttu-id="59e42-130">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="59e42-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="59e42-131">筆記</span><span class="sxs-lookup"><span data-stu-id="59e42-131">NOTES</span></span>

## <span data-ttu-id="59e42-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="59e42-132">RELATED LINKS</span></span>
