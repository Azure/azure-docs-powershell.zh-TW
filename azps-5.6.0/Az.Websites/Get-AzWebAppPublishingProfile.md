---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 512162485b38d6cf02ad8519131eb4252605c4a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913290"
---
# <span data-ttu-id="f30b2-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="f30b2-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="f30b2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f30b2-102">SYNOPSIS</span></span>
<span data-ttu-id="f30b2-103">獲得 Azure Web App 發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="f30b2-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="f30b2-104">語法</span><span class="sxs-lookup"><span data-stu-id="f30b2-104">SYNTAX</span></span>

### <span data-ttu-id="f30b2-105">S1</span><span class="sxs-lookup"><span data-stu-id="f30b2-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f30b2-106">S2</span><span class="sxs-lookup"><span data-stu-id="f30b2-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f30b2-107">描述</span><span class="sxs-lookup"><span data-stu-id="f30b2-107">DESCRIPTION</span></span>
<span data-ttu-id="f30b2-108">**Get-AzWebAppPublishingProfile** Cmdlet 會取得 Azure Web App 發佈設定檔。</span><span class="sxs-lookup"><span data-stu-id="f30b2-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="f30b2-109">例子</span><span class="sxs-lookup"><span data-stu-id="f30b2-109">EXAMPLES</span></span>

### <span data-ttu-id="f30b2-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="f30b2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile.publishsettings"
```

<span data-ttu-id="f30b2-111">此命令會以 Ftp 格式為 Web App ContosoWebApp 的發佈設定檔，與資源群組 Default-Web-WestUS 相關聯，並儲存在指定的輸出檔案中。</span><span class="sxs-lookup"><span data-stu-id="f30b2-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="f30b2-112">參數</span><span class="sxs-lookup"><span data-stu-id="f30b2-112">PARAMETERS</span></span>

### <span data-ttu-id="f30b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f30b2-113">-DefaultProfile</span></span>
<span data-ttu-id="f30b2-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f30b2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f30b2-115">-格式</span><span class="sxs-lookup"><span data-stu-id="f30b2-115">-Format</span></span>
<span data-ttu-id="f30b2-116">格式</span><span class="sxs-lookup"><span data-stu-id="f30b2-116">Format</span></span>

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

### <span data-ttu-id="f30b2-117">-IncludeDsterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="f30b2-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="f30b2-118">如果為 True，請包含災害復原端點</span><span class="sxs-lookup"><span data-stu-id="f30b2-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="f30b2-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f30b2-119">-Name</span></span>
<span data-ttu-id="f30b2-120">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="f30b2-120">WebApp Name</span></span>

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

### <span data-ttu-id="f30b2-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="f30b2-121">-OutputFile</span></span>
<span data-ttu-id="f30b2-122">輸出檔案</span><span class="sxs-lookup"><span data-stu-id="f30b2-122">Output File</span></span>

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

### <span data-ttu-id="f30b2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f30b2-123">-ResourceGroupName</span></span>
<span data-ttu-id="f30b2-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="f30b2-124">Resource Group Name</span></span>

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

### <span data-ttu-id="f30b2-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f30b2-125">-WebApp</span></span>
<span data-ttu-id="f30b2-126">WebApp 物件</span><span class="sxs-lookup"><span data-stu-id="f30b2-126">WebApp Object</span></span>

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

### <span data-ttu-id="f30b2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f30b2-127">CommonParameters</span></span>
<span data-ttu-id="f30b2-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f30b2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f30b2-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f30b2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f30b2-130">輸入</span><span class="sxs-lookup"><span data-stu-id="f30b2-130">INPUTS</span></span>

### <span data-ttu-id="f30b2-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f30b2-131">System.String</span></span>

### <span data-ttu-id="f30b2-132">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="f30b2-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f30b2-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f30b2-133">OUTPUTS</span></span>

### <span data-ttu-id="f30b2-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f30b2-134">System.String</span></span>

## <span data-ttu-id="f30b2-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f30b2-135">NOTES</span></span>

## <span data-ttu-id="f30b2-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f30b2-136">RELATED LINKS</span></span>

[<span data-ttu-id="f30b2-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="f30b2-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="f30b2-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f30b2-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


