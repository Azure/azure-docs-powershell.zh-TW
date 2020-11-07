---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackuplist
schema: 2.0.0
ms.openlocfilehash: ef409c62d56a95d36f1e7c9a02018b281c00e3c9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800266"
---
# <span data-ttu-id="7f473-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="7f473-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="7f473-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f473-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f473-103">句法</span><span class="sxs-lookup"><span data-stu-id="7f473-103">SYNTAX</span></span>

### <span data-ttu-id="7f473-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="7f473-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f473-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="7f473-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f473-106">說明</span><span class="sxs-lookup"><span data-stu-id="7f473-106">DESCRIPTION</span></span>
<span data-ttu-id="7f473-107">**AzureRmWebAppBackupList** Cmdlet 會取得 Azure Web App 備份的清單。</span><span class="sxs-lookup"><span data-stu-id="7f473-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="7f473-108">示例</span><span class="sxs-lookup"><span data-stu-id="7f473-108">EXAMPLES</span></span>

### <span data-ttu-id="7f473-109">sr-1</span><span class="sxs-lookup"><span data-stu-id="7f473-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="7f473-110">這個命令會傳回與資源群組 ContosoResourceGroup 相關聯之 WebApp WebAppStandard 的備份清單。</span><span class="sxs-lookup"><span data-stu-id="7f473-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="7f473-111">參數</span><span class="sxs-lookup"><span data-stu-id="7f473-111">PARAMETERS</span></span>

### <span data-ttu-id="7f473-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f473-112">-DefaultProfile</span></span>
<span data-ttu-id="7f473-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f473-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f473-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="7f473-114">-Name</span></span>
<span data-ttu-id="7f473-115">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="7f473-115">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f473-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f473-116">-ResourceGroupName</span></span>
<span data-ttu-id="7f473-117">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="7f473-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f473-118">-槽</span><span class="sxs-lookup"><span data-stu-id="7f473-118">-Slot</span></span>
<span data-ttu-id="7f473-119">槽名稱</span><span class="sxs-lookup"><span data-stu-id="7f473-119">Slot name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f473-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7f473-120">-WebApp</span></span>
<span data-ttu-id="7f473-121">管道 WebApp</span><span class="sxs-lookup"><span data-stu-id="7f473-121">Piped WebApp</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f473-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f473-122">CommonParameters</span></span>
<span data-ttu-id="7f473-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f473-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f473-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7f473-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f473-125">輸入</span><span class="sxs-lookup"><span data-stu-id="7f473-125">INPUTS</span></span>

### <span data-ttu-id="7f473-126">網站地圖</span><span class="sxs-lookup"><span data-stu-id="7f473-126">Site</span></span>
<span data-ttu-id="7f473-127">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="7f473-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="7f473-128">輸出</span><span class="sxs-lookup"><span data-stu-id="7f473-128">OUTPUTS</span></span>

### <span data-ttu-id="7f473-129">AzureWebAppBackup []. WebApps [WebApps]</span><span class="sxs-lookup"><span data-stu-id="7f473-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="7f473-130">筆記</span><span class="sxs-lookup"><span data-stu-id="7f473-130">NOTES</span></span>

## <span data-ttu-id="7f473-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f473-131">RELATED LINKS</span></span>

