---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: a59d747dd7ba91d69d364770c91baf1a21ffedd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448152"
---
# <span data-ttu-id="5980c-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="5980c-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="5980c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5980c-102">SYNOPSIS</span></span>
<span data-ttu-id="5980c-103">取得 Azure Web App 發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="5980c-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5980c-104">句法</span><span class="sxs-lookup"><span data-stu-id="5980c-104">SYNTAX</span></span>

### <span data-ttu-id="5980c-105">S1</span><span class="sxs-lookup"><span data-stu-id="5980c-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5980c-106">S2</span><span class="sxs-lookup"><span data-stu-id="5980c-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5980c-107">說明</span><span class="sxs-lookup"><span data-stu-id="5980c-107">DESCRIPTION</span></span>
<span data-ttu-id="5980c-108">**AzureRmWebAppPublishingProfile** Cmdlet 會取得 Azure Web App 發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="5980c-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="5980c-109">示例</span><span class="sxs-lookup"><span data-stu-id="5980c-109">EXAMPLES</span></span>

### <span data-ttu-id="5980c-110">sr-1</span><span class="sxs-lookup"><span data-stu-id="5980c-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="5980c-111">這個命令會針對與資源群組預設-Web WestUS 相關聯的 Web App ContosoWebApp，取得 Ftp 格式的發佈設定檔，並將它儲存在指定的輸出檔案中。</span><span class="sxs-lookup"><span data-stu-id="5980c-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="5980c-112">參數</span><span class="sxs-lookup"><span data-stu-id="5980c-112">PARAMETERS</span></span>

### <span data-ttu-id="5980c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5980c-113">-DefaultProfile</span></span>
<span data-ttu-id="5980c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5980c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5980c-115">-Format</span><span class="sxs-lookup"><span data-stu-id="5980c-115">-Format</span></span>
<span data-ttu-id="5980c-116">設置</span><span class="sxs-lookup"><span data-stu-id="5980c-116">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5980c-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="5980c-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="5980c-118">如果 true，則包含災害復原端點</span><span class="sxs-lookup"><span data-stu-id="5980c-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5980c-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="5980c-119">-Name</span></span>
<span data-ttu-id="5980c-120">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="5980c-120">WebApp Name</span></span>

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

### <span data-ttu-id="5980c-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="5980c-121">-OutputFile</span></span>
<span data-ttu-id="5980c-122">輸出檔案</span><span class="sxs-lookup"><span data-stu-id="5980c-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5980c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5980c-123">-ResourceGroupName</span></span>
<span data-ttu-id="5980c-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="5980c-124">Resource Group Name</span></span>

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

### <span data-ttu-id="5980c-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5980c-125">-WebApp</span></span>
<span data-ttu-id="5980c-126">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="5980c-126">WebApp Object</span></span>

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

### <span data-ttu-id="5980c-127">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="5980c-127">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="5980c-128">如果 true，則包含災害復原端點</span><span class="sxs-lookup"><span data-stu-id="5980c-128">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5980c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5980c-129">CommonParameters</span></span>
<span data-ttu-id="5980c-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5980c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5980c-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5980c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5980c-132">輸入</span><span class="sxs-lookup"><span data-stu-id="5980c-132">INPUTS</span></span>

### <span data-ttu-id="5980c-133">System.object</span><span class="sxs-lookup"><span data-stu-id="5980c-133">System.String</span></span>

### <span data-ttu-id="5980c-134">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="5980c-134">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="5980c-135">參數： WebApp (ByValue) </span><span class="sxs-lookup"><span data-stu-id="5980c-135">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="5980c-136">輸出</span><span class="sxs-lookup"><span data-stu-id="5980c-136">OUTPUTS</span></span>

### <span data-ttu-id="5980c-137">System.object</span><span class="sxs-lookup"><span data-stu-id="5980c-137">System.String</span></span>

## <span data-ttu-id="5980c-138">筆記</span><span class="sxs-lookup"><span data-stu-id="5980c-138">NOTES</span></span>

## <span data-ttu-id="5980c-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="5980c-139">RELATED LINKS</span></span>

[<span data-ttu-id="5980c-140">AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5980c-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="5980c-141">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="5980c-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


