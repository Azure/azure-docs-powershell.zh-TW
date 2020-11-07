---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: 508aa5245d56af85136ee475a420819d8224b491
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793324"
---
# <span data-ttu-id="77696-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="77696-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="77696-102">摘要</span><span class="sxs-lookup"><span data-stu-id="77696-102">SYNOPSIS</span></span>

## <span data-ttu-id="77696-103">句法</span><span class="sxs-lookup"><span data-stu-id="77696-103">SYNTAX</span></span>

### <span data-ttu-id="77696-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="77696-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77696-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="77696-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77696-106">說明</span><span class="sxs-lookup"><span data-stu-id="77696-106">DESCRIPTION</span></span>
<span data-ttu-id="77696-107">**AzWebAppBackup** Cmdlet 會移除 Azure Web App 的指定備份。</span><span class="sxs-lookup"><span data-stu-id="77696-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="77696-108">示例</span><span class="sxs-lookup"><span data-stu-id="77696-108">EXAMPLES</span></span>

### <span data-ttu-id="77696-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="77696-109">1:</span></span>
```
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="77696-110">這個命令會從屬於資源群組 Default-Web WestUS 的名為「WebAppStandard」的 Web App 中，移除 ID 為「12345」的備份。</span><span class="sxs-lookup"><span data-stu-id="77696-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="77696-111">參數</span><span class="sxs-lookup"><span data-stu-id="77696-111">PARAMETERS</span></span>

### <span data-ttu-id="77696-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="77696-112">-BackupId</span></span>
<span data-ttu-id="77696-113">備份識別碼</span><span class="sxs-lookup"><span data-stu-id="77696-113">Backup Id</span></span>

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

### <span data-ttu-id="77696-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77696-114">-DefaultProfile</span></span>
<span data-ttu-id="77696-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="77696-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77696-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="77696-116">-Name</span></span>
<span data-ttu-id="77696-117">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="77696-117">WebApp Name</span></span>

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

### <span data-ttu-id="77696-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77696-118">-ResourceGroupName</span></span>
<span data-ttu-id="77696-119">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="77696-119">Resource Group Name</span></span>

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

### <span data-ttu-id="77696-120">-槽</span><span class="sxs-lookup"><span data-stu-id="77696-120">-Slot</span></span>
<span data-ttu-id="77696-121">WebApp 槽名稱</span><span class="sxs-lookup"><span data-stu-id="77696-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="77696-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="77696-122">-WebApp</span></span>
<span data-ttu-id="77696-123">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="77696-123">WebApp Object</span></span>

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

### <span data-ttu-id="77696-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77696-124">CommonParameters</span></span>
<span data-ttu-id="77696-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="77696-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77696-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="77696-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77696-127">輸入</span><span class="sxs-lookup"><span data-stu-id="77696-127">INPUTS</span></span>

### <span data-ttu-id="77696-128">System.object</span><span class="sxs-lookup"><span data-stu-id="77696-128">System.String</span></span>

### <span data-ttu-id="77696-129">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="77696-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="77696-130">輸出</span><span class="sxs-lookup"><span data-stu-id="77696-130">OUTPUTS</span></span>

### <span data-ttu-id="77696-131">BackupItem 中的 [網站]。</span><span class="sxs-lookup"><span data-stu-id="77696-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="77696-132">筆記</span><span class="sxs-lookup"><span data-stu-id="77696-132">NOTES</span></span>

## <span data-ttu-id="77696-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="77696-133">RELATED LINKS</span></span>
