---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: 104614bd0fdd2ca8555765a301f6b257cdac0bc7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797401"
---
# <span data-ttu-id="1b158-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="1b158-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="1b158-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b158-102">SYNOPSIS</span></span>

## <span data-ttu-id="1b158-103">句法</span><span class="sxs-lookup"><span data-stu-id="1b158-103">SYNTAX</span></span>

### <span data-ttu-id="1b158-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1b158-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b158-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1b158-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b158-106">說明</span><span class="sxs-lookup"><span data-stu-id="1b158-106">DESCRIPTION</span></span>
<span data-ttu-id="1b158-107">**AzWebAppBackupList** Cmdlet 會取得 Azure Web App 備份的清單。</span><span class="sxs-lookup"><span data-stu-id="1b158-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="1b158-108">示例</span><span class="sxs-lookup"><span data-stu-id="1b158-108">EXAMPLES</span></span>

### <span data-ttu-id="1b158-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="1b158-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="1b158-110">這個命令會傳回與資源群組 ContosoResourceGroup 相關聯之 WebApp WebAppStandard 的備份清單。</span><span class="sxs-lookup"><span data-stu-id="1b158-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="1b158-111">參數</span><span class="sxs-lookup"><span data-stu-id="1b158-111">PARAMETERS</span></span>

### <span data-ttu-id="1b158-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b158-112">-DefaultProfile</span></span>
<span data-ttu-id="1b158-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b158-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b158-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="1b158-114">-Name</span></span>
<span data-ttu-id="1b158-115">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="1b158-115">WebApp Name</span></span>

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

### <span data-ttu-id="1b158-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b158-116">-ResourceGroupName</span></span>
<span data-ttu-id="1b158-117">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="1b158-117">Resource Group Name</span></span>

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

### <span data-ttu-id="1b158-118">-槽</span><span class="sxs-lookup"><span data-stu-id="1b158-118">-Slot</span></span>
<span data-ttu-id="1b158-119">槽名稱</span><span class="sxs-lookup"><span data-stu-id="1b158-119">Slot name</span></span>

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

### <span data-ttu-id="1b158-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1b158-120">-WebApp</span></span>
<span data-ttu-id="1b158-121">管道 WebApp</span><span class="sxs-lookup"><span data-stu-id="1b158-121">Piped WebApp</span></span>

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

### <span data-ttu-id="1b158-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b158-122">CommonParameters</span></span>
<span data-ttu-id="1b158-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b158-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b158-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b158-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b158-125">輸入</span><span class="sxs-lookup"><span data-stu-id="1b158-125">INPUTS</span></span>

### <span data-ttu-id="1b158-126">System.object</span><span class="sxs-lookup"><span data-stu-id="1b158-126">System.String</span></span>

### <span data-ttu-id="1b158-127">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="1b158-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1b158-128">輸出</span><span class="sxs-lookup"><span data-stu-id="1b158-128">OUTPUTS</span></span>

### <span data-ttu-id="1b158-129">WebApps WebApps. AzureWebAppBackup （）</span><span class="sxs-lookup"><span data-stu-id="1b158-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="1b158-130">筆記</span><span class="sxs-lookup"><span data-stu-id="1b158-130">NOTES</span></span>

## <span data-ttu-id="1b158-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b158-131">RELATED LINKS</span></span>
