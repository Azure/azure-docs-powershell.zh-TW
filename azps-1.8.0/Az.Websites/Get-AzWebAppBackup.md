---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: 30f1581ddd4668fbe4d4d4b6d8c902f6aac929ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614305"
---
# <span data-ttu-id="b799f-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="b799f-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="b799f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b799f-102">SYNOPSIS</span></span>

## <span data-ttu-id="b799f-103">句法</span><span class="sxs-lookup"><span data-stu-id="b799f-103">SYNTAX</span></span>

### <span data-ttu-id="b799f-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="b799f-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b799f-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="b799f-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b799f-106">說明</span><span class="sxs-lookup"><span data-stu-id="b799f-106">DESCRIPTION</span></span>
<span data-ttu-id="b799f-107">**AzWebAppBackup** Cmdlet 會取得 Azure Web App 的指定備份。</span><span class="sxs-lookup"><span data-stu-id="b799f-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="b799f-108">示例</span><span class="sxs-lookup"><span data-stu-id="b799f-108">EXAMPLES</span></span>

### <span data-ttu-id="b799f-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="b799f-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="b799f-110">這個命令會從屬於資源群組 Default-Web WestUS 的名為「WebAppStandard」的 Web App 中，取得 ID 為「12345」的備份。</span><span class="sxs-lookup"><span data-stu-id="b799f-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="b799f-111">參數</span><span class="sxs-lookup"><span data-stu-id="b799f-111">PARAMETERS</span></span>

### <span data-ttu-id="b799f-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="b799f-112">-BackupId</span></span>
<span data-ttu-id="b799f-113">備份識別碼</span><span class="sxs-lookup"><span data-stu-id="b799f-113">Backup Id</span></span>

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

### <span data-ttu-id="b799f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b799f-114">-DefaultProfile</span></span>
<span data-ttu-id="b799f-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b799f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b799f-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="b799f-116">-Name</span></span>
<span data-ttu-id="b799f-117">Webapp 名稱</span><span class="sxs-lookup"><span data-stu-id="b799f-117">Webapp Name</span></span>

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

### <span data-ttu-id="b799f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b799f-118">-ResourceGroupName</span></span>
<span data-ttu-id="b799f-119">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b799f-119">Resource Group Name</span></span>

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

### <span data-ttu-id="b799f-120">-槽</span><span class="sxs-lookup"><span data-stu-id="b799f-120">-Slot</span></span>
<span data-ttu-id="b799f-121">槽名稱</span><span class="sxs-lookup"><span data-stu-id="b799f-121">Slot Name</span></span>

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

### <span data-ttu-id="b799f-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b799f-122">-WebApp</span></span>
<span data-ttu-id="b799f-123">管道 WebApp</span><span class="sxs-lookup"><span data-stu-id="b799f-123">Piped WebApp</span></span>

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

### <span data-ttu-id="b799f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b799f-124">CommonParameters</span></span>
<span data-ttu-id="b799f-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b799f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b799f-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b799f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b799f-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b799f-127">INPUTS</span></span>

### <span data-ttu-id="b799f-128">System.object</span><span class="sxs-lookup"><span data-stu-id="b799f-128">System.String</span></span>

### <span data-ttu-id="b799f-129">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="b799f-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="b799f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="b799f-130">OUTPUTS</span></span>

### <span data-ttu-id="b799f-131">WebApps WebApps. AzureWebAppBackup （）</span><span class="sxs-lookup"><span data-stu-id="b799f-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="b799f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="b799f-132">NOTES</span></span>

## <span data-ttu-id="b799f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="b799f-133">RELATED LINKS</span></span>
