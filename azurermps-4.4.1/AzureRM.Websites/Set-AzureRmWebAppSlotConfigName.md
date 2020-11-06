---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 3ed7bd25c394c2bef5cb3636a4f8c238f45a3558
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444864"
---
# <span data-ttu-id="2b675-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="2b675-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="2b675-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b675-102">SYNOPSIS</span></span>
<span data-ttu-id="2b675-103">設定 Web 應用程式槽配置名稱</span><span class="sxs-lookup"><span data-stu-id="2b675-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b675-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b675-104">SYNTAX</span></span>

### <span data-ttu-id="2b675-105">S1</span><span class="sxs-lookup"><span data-stu-id="2b675-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b675-106">S2</span><span class="sxs-lookup"><span data-stu-id="2b675-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b675-107">說明</span><span class="sxs-lookup"><span data-stu-id="2b675-107">DESCRIPTION</span></span>
<span data-ttu-id="2b675-108">**AzureRmWebAppSlotConfigName** Cmdlet 會將 App 設定和連接字串標示為槽設定</span><span class="sxs-lookup"><span data-stu-id="2b675-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="2b675-109">示例</span><span class="sxs-lookup"><span data-stu-id="2b675-109">EXAMPLES</span></span>

### <span data-ttu-id="2b675-110">sr-1</span><span class="sxs-lookup"><span data-stu-id="2b675-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="2b675-111">這個命令會移除與資源群組預設-Web-WestUS 相關聯之 Web App ContosoWebApp 的所有 app 設定和連線字串。</span><span class="sxs-lookup"><span data-stu-id="2b675-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="2b675-112">參數</span><span class="sxs-lookup"><span data-stu-id="2b675-112">PARAMETERS</span></span>

### <span data-ttu-id="2b675-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="2b675-113">-AppSettingNames</span></span>
<span data-ttu-id="2b675-114">應用程式設定名稱字串陣列</span><span class="sxs-lookup"><span data-stu-id="2b675-114">App Settings Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b675-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="2b675-115">-ConnectionStringNames</span></span>
<span data-ttu-id="2b675-116">連接字串名稱字串陣列</span><span class="sxs-lookup"><span data-stu-id="2b675-116">Connection String Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b675-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="2b675-117">-Name</span></span>
<span data-ttu-id="2b675-118">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="2b675-118">WebApp Name</span></span>

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

### <span data-ttu-id="2b675-119">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="2b675-119">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="2b675-120">[移除所有 App 設定名稱] 選項</span><span class="sxs-lookup"><span data-stu-id="2b675-120">Remove All App Setting Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b675-121">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="2b675-121">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="2b675-122">[移除所有連線字串名稱] 選項</span><span class="sxs-lookup"><span data-stu-id="2b675-122">Remove All Connection String Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b675-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b675-123">-ResourceGroupName</span></span>
<span data-ttu-id="2b675-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="2b675-124">Resource Group Name</span></span>

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

### <span data-ttu-id="2b675-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2b675-125">-WebApp</span></span>
<span data-ttu-id="2b675-126">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="2b675-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b675-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b675-127">-DefaultProfile</span></span>
<span data-ttu-id="2b675-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b675-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b675-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b675-129">CommonParameters</span></span>
<span data-ttu-id="2b675-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b675-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b675-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2b675-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b675-132">輸入</span><span class="sxs-lookup"><span data-stu-id="2b675-132">INPUTS</span></span>

### <span data-ttu-id="2b675-133">網站地圖</span><span class="sxs-lookup"><span data-stu-id="2b675-133">Site</span></span>
<span data-ttu-id="2b675-134">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="2b675-134">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2b675-135">輸出</span><span class="sxs-lookup"><span data-stu-id="2b675-135">OUTPUTS</span></span>

## <span data-ttu-id="2b675-136">筆記</span><span class="sxs-lookup"><span data-stu-id="2b675-136">NOTES</span></span>

## <span data-ttu-id="2b675-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b675-137">RELATED LINKS</span></span>

