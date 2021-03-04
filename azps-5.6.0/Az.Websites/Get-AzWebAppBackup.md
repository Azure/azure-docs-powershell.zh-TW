---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: 70dea111b2fc48e2d5063db21dd53a6e9ca76f75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909873"
---
# <span data-ttu-id="435d7-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="435d7-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="435d7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="435d7-102">SYNOPSIS</span></span>

## <span data-ttu-id="435d7-103">語法</span><span class="sxs-lookup"><span data-stu-id="435d7-103">SYNTAX</span></span>

### <span data-ttu-id="435d7-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="435d7-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="435d7-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="435d7-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="435d7-106">描述</span><span class="sxs-lookup"><span data-stu-id="435d7-106">DESCRIPTION</span></span>
<span data-ttu-id="435d7-107">**Get-AzWebAppBackup** Cmdlet 會取得 Azure Web App 的指定備份。</span><span class="sxs-lookup"><span data-stu-id="435d7-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="435d7-108">例子</span><span class="sxs-lookup"><span data-stu-id="435d7-108">EXAMPLES</span></span>

### <span data-ttu-id="435d7-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="435d7-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="435d7-110">此命令會從屬於資源群組 Default-Web-WestUS 的 Web App 中，使用識別碼 "12345" 的 Web App 進行備份。</span><span class="sxs-lookup"><span data-stu-id="435d7-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="435d7-111">參數</span><span class="sxs-lookup"><span data-stu-id="435d7-111">PARAMETERS</span></span>

### <span data-ttu-id="435d7-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="435d7-112">-BackupId</span></span>
<span data-ttu-id="435d7-113">備份識別碼</span><span class="sxs-lookup"><span data-stu-id="435d7-113">Backup Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="435d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="435d7-114">-DefaultProfile</span></span>
<span data-ttu-id="435d7-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="435d7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="435d7-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="435d7-116">-Name</span></span>
<span data-ttu-id="435d7-117">Webapp 名稱</span><span class="sxs-lookup"><span data-stu-id="435d7-117">Webapp Name</span></span>

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

### <span data-ttu-id="435d7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="435d7-118">-ResourceGroupName</span></span>
<span data-ttu-id="435d7-119">資源組名</span><span class="sxs-lookup"><span data-stu-id="435d7-119">Resource Group Name</span></span>

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

### <span data-ttu-id="435d7-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="435d7-120">-Slot</span></span>
<span data-ttu-id="435d7-121">插槽名稱</span><span class="sxs-lookup"><span data-stu-id="435d7-121">Slot Name</span></span>

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

### <span data-ttu-id="435d7-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="435d7-122">-WebApp</span></span>
<span data-ttu-id="435d7-123">管道 WebApp</span><span class="sxs-lookup"><span data-stu-id="435d7-123">Piped WebApp</span></span>

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

### <span data-ttu-id="435d7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="435d7-124">CommonParameters</span></span>
<span data-ttu-id="435d7-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="435d7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="435d7-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="435d7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="435d7-127">輸入</span><span class="sxs-lookup"><span data-stu-id="435d7-127">INPUTS</span></span>

### <span data-ttu-id="435d7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="435d7-128">System.String</span></span>

### <span data-ttu-id="435d7-129">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="435d7-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="435d7-130">輸出</span><span class="sxs-lookup"><span data-stu-id="435d7-130">OUTPUTS</span></span>

### <span data-ttu-id="435d7-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="435d7-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="435d7-132">筆記</span><span class="sxs-lookup"><span data-stu-id="435d7-132">NOTES</span></span>

## <span data-ttu-id="435d7-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="435d7-133">RELATED LINKS</span></span>
