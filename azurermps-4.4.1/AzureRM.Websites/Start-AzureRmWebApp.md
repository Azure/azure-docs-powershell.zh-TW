---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Start-AzureRmWebApp.md
ms.openlocfilehash: 20acba9bc0f08857c9bdfaaf559544f26b4902ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444863"
---
# <span data-ttu-id="39762-101">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="39762-101">Start-AzureRmWebApp</span></span>

## <span data-ttu-id="39762-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39762-102">SYNOPSIS</span></span>
<span data-ttu-id="39762-103">啟動 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="39762-103">Starts an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39762-104">句法</span><span class="sxs-lookup"><span data-stu-id="39762-104">SYNTAX</span></span>

### <span data-ttu-id="39762-105">S1</span><span class="sxs-lookup"><span data-stu-id="39762-105">S1</span></span>
```
Start-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="39762-106">S2</span><span class="sxs-lookup"><span data-stu-id="39762-106">S2</span></span>
```
Start-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39762-107">說明</span><span class="sxs-lookup"><span data-stu-id="39762-107">DESCRIPTION</span></span>
<span data-ttu-id="39762-108">**AzureRmWebApp** Cmdlet 會啟動 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="39762-108">The **Start-AzureRmWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="39762-109">示例</span><span class="sxs-lookup"><span data-stu-id="39762-109">EXAMPLES</span></span>

### <span data-ttu-id="39762-110">範例1：啟動 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="39762-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="39762-111">這個命令會啟動名為 ContosoWebApp 的 Web App，該應用程式屬於名為「預設-Web-WestUS」的資源群組。</span><span class="sxs-lookup"><span data-stu-id="39762-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="39762-112">參數</span><span class="sxs-lookup"><span data-stu-id="39762-112">PARAMETERS</span></span>

### <span data-ttu-id="39762-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="39762-113">-Name</span></span>
<span data-ttu-id="39762-114">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="39762-114">WebApp Name</span></span>

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

### <span data-ttu-id="39762-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39762-115">-ResourceGroupName</span></span>
<span data-ttu-id="39762-116">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="39762-116">Resource Group Name</span></span>

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

### <span data-ttu-id="39762-117">-WebApp</span><span class="sxs-lookup"><span data-stu-id="39762-117">-WebApp</span></span>
<span data-ttu-id="39762-118">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="39762-118">WebApp Object</span></span>

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

### <span data-ttu-id="39762-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39762-119">-DefaultProfile</span></span>
<span data-ttu-id="39762-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="39762-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39762-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39762-121">CommonParameters</span></span>
<span data-ttu-id="39762-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39762-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39762-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="39762-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39762-124">輸入</span><span class="sxs-lookup"><span data-stu-id="39762-124">INPUTS</span></span>

### <span data-ttu-id="39762-125">網站地圖</span><span class="sxs-lookup"><span data-stu-id="39762-125">Site</span></span>
<span data-ttu-id="39762-126">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="39762-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="39762-127">輸出</span><span class="sxs-lookup"><span data-stu-id="39762-127">OUTPUTS</span></span>

## <span data-ttu-id="39762-128">筆記</span><span class="sxs-lookup"><span data-stu-id="39762-128">NOTES</span></span>

## <span data-ttu-id="39762-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="39762-129">RELATED LINKS</span></span>

[<span data-ttu-id="39762-130">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="39762-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="39762-131">新-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="39762-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="39762-132">移除-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="39762-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="39762-133">重新開機-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="39762-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="39762-134">停止 AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="39762-134">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


