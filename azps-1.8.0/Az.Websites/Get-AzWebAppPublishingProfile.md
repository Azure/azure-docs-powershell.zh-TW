---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: a89ebd3142d738664cd80cab198bd6f791c1287a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614295"
---
# <span data-ttu-id="dc244-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="dc244-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="dc244-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc244-102">SYNOPSIS</span></span>
<span data-ttu-id="dc244-103">取得 Azure Web App 發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="dc244-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="dc244-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc244-104">SYNTAX</span></span>

### <span data-ttu-id="dc244-105">S1</span><span class="sxs-lookup"><span data-stu-id="dc244-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc244-106">S2</span><span class="sxs-lookup"><span data-stu-id="dc244-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc244-107">說明</span><span class="sxs-lookup"><span data-stu-id="dc244-107">DESCRIPTION</span></span>
<span data-ttu-id="dc244-108">**AzWebAppPublishingProfile** Cmdlet 會取得 Azure Web App 發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="dc244-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="dc244-109">示例</span><span class="sxs-lookup"><span data-stu-id="dc244-109">EXAMPLES</span></span>

### <span data-ttu-id="dc244-110">sr-1</span><span class="sxs-lookup"><span data-stu-id="dc244-110">1:</span></span>
```
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="dc244-111">這個命令會針對與資源群組預設-Web WestUS 相關聯的 Web App ContosoWebApp，取得 Ftp 格式的發佈設定檔，並將它儲存在指定的輸出檔案中。</span><span class="sxs-lookup"><span data-stu-id="dc244-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="dc244-112">參數</span><span class="sxs-lookup"><span data-stu-id="dc244-112">PARAMETERS</span></span>

### <span data-ttu-id="dc244-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc244-113">-DefaultProfile</span></span>
<span data-ttu-id="dc244-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc244-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc244-115">-Format</span><span class="sxs-lookup"><span data-stu-id="dc244-115">-Format</span></span>
<span data-ttu-id="dc244-116">設置</span><span class="sxs-lookup"><span data-stu-id="dc244-116">Format</span></span>

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

### <span data-ttu-id="dc244-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="dc244-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="dc244-118">如果 true，則包含災害復原端點</span><span class="sxs-lookup"><span data-stu-id="dc244-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc244-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="dc244-119">-Name</span></span>
<span data-ttu-id="dc244-120">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="dc244-120">WebApp Name</span></span>

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

### <span data-ttu-id="dc244-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="dc244-121">-OutputFile</span></span>
<span data-ttu-id="dc244-122">輸出檔案</span><span class="sxs-lookup"><span data-stu-id="dc244-122">Output File</span></span>

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

### <span data-ttu-id="dc244-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc244-123">-ResourceGroupName</span></span>
<span data-ttu-id="dc244-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="dc244-124">Resource Group Name</span></span>

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

### <span data-ttu-id="dc244-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="dc244-125">-WebApp</span></span>
<span data-ttu-id="dc244-126">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="dc244-126">WebApp Object</span></span>

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

### <span data-ttu-id="dc244-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc244-127">CommonParameters</span></span>
<span data-ttu-id="dc244-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc244-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc244-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dc244-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc244-130">輸入</span><span class="sxs-lookup"><span data-stu-id="dc244-130">INPUTS</span></span>

### <span data-ttu-id="dc244-131">System.object</span><span class="sxs-lookup"><span data-stu-id="dc244-131">System.String</span></span>

### <span data-ttu-id="dc244-132">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="dc244-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="dc244-133">輸出</span><span class="sxs-lookup"><span data-stu-id="dc244-133">OUTPUTS</span></span>

### <span data-ttu-id="dc244-134">System.object</span><span class="sxs-lookup"><span data-stu-id="dc244-134">System.String</span></span>

## <span data-ttu-id="dc244-135">筆記</span><span class="sxs-lookup"><span data-stu-id="dc244-135">NOTES</span></span>

## <span data-ttu-id="dc244-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc244-136">RELATED LINKS</span></span>

[<span data-ttu-id="dc244-137">AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="dc244-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="dc244-138">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dc244-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


