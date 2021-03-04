---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 00df9069400a1d3e2ae10abfb03d9d55bff08735
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907014"
---
# <span data-ttu-id="a1146-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1146-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="a1146-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a1146-102">SYNOPSIS</span></span>

## <span data-ttu-id="a1146-103">語法</span><span class="sxs-lookup"><span data-stu-id="a1146-103">SYNTAX</span></span>

### <span data-ttu-id="a1146-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="a1146-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1146-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="a1146-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1146-106">描述</span><span class="sxs-lookup"><span data-stu-id="a1146-106">DESCRIPTION</span></span>
<span data-ttu-id="a1146-107">**Get-AzWebAppBackupConfiguration** Cmdlet 取得 Azure Web App 的備份群組原則。</span><span class="sxs-lookup"><span data-stu-id="a1146-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="a1146-108">例子</span><span class="sxs-lookup"><span data-stu-id="a1146-108">EXAMPLES</span></span>

### <span data-ttu-id="a1146-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="a1146-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="a1146-110">此命令會從名稱為 WebAppStandard 的 Web App 中，從屬於資源群組 Default-Web-WestUS 的備份組。</span><span class="sxs-lookup"><span data-stu-id="a1146-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a1146-111">參數</span><span class="sxs-lookup"><span data-stu-id="a1146-111">PARAMETERS</span></span>

### <span data-ttu-id="a1146-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1146-112">-DefaultProfile</span></span>
<span data-ttu-id="a1146-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1146-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1146-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="a1146-114">-Name</span></span>
<span data-ttu-id="a1146-115">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="a1146-115">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1146-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1146-116">-ResourceGroupName</span></span>
<span data-ttu-id="a1146-117">資源組名</span><span class="sxs-lookup"><span data-stu-id="a1146-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1146-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="a1146-118">-Slot</span></span>
<span data-ttu-id="a1146-119">插槽名稱</span><span class="sxs-lookup"><span data-stu-id="a1146-119">Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1146-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a1146-120">-WebApp</span></span>
<span data-ttu-id="a1146-121">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="a1146-121">WebApp Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1146-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1146-122">CommonParameters</span></span>
<span data-ttu-id="a1146-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a1146-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1146-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a1146-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1146-125">輸入</span><span class="sxs-lookup"><span data-stu-id="a1146-125">INPUTS</span></span>

### <span data-ttu-id="a1146-126">System.String</span><span class="sxs-lookup"><span data-stu-id="a1146-126">System.String</span></span>

### <span data-ttu-id="a1146-127">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="a1146-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a1146-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a1146-128">OUTPUTS</span></span>

### <span data-ttu-id="a1146-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="a1146-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="a1146-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a1146-130">NOTES</span></span>

## <span data-ttu-id="a1146-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1146-131">RELATED LINKS</span></span>
