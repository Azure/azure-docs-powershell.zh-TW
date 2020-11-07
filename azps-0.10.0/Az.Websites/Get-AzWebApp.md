---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebApp.md
ms.openlocfilehash: f86e0f18c7d793b5876a48c39b56b11c14b17546
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795001"
---
# <span data-ttu-id="4e832-101">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4e832-101">Get-AzWebApp</span></span>

## <span data-ttu-id="4e832-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e832-102">SYNOPSIS</span></span>
<span data-ttu-id="4e832-103">在指定的資源群組中取得 Azure Web Apps。</span><span class="sxs-lookup"><span data-stu-id="4e832-103">Gets Azure Web Apps in the specified resource group.</span></span>

## <span data-ttu-id="4e832-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e832-104">SYNTAX</span></span>

### <span data-ttu-id="4e832-105">S1</span><span class="sxs-lookup"><span data-stu-id="4e832-105">S1</span></span>
```
Get-AzWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e832-106">S2</span><span class="sxs-lookup"><span data-stu-id="4e832-106">S2</span></span>
```
Get-AzWebApp [-AppServicePlan] <AppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e832-107">S3</span><span class="sxs-lookup"><span data-stu-id="4e832-107">S3</span></span>
```
Get-AzWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e832-108">說明</span><span class="sxs-lookup"><span data-stu-id="4e832-108">DESCRIPTION</span></span>
<span data-ttu-id="4e832-109">**AzWebApp** Cmdlet 會取得 Azure Web App 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4e832-109">The **Get-AzWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="4e832-110">示例</span><span class="sxs-lookup"><span data-stu-id="4e832-110">EXAMPLES</span></span>

### <span data-ttu-id="4e832-111">範例1：從資源群組取得 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="4e832-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="4e832-112">這個命令會取得屬於資源群組 Default-Web WestUS 的名為 ContosoSite 的 Web App。</span><span class="sxs-lookup"><span data-stu-id="4e832-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="4e832-113">參數</span><span class="sxs-lookup"><span data-stu-id="4e832-113">PARAMETERS</span></span>

### <span data-ttu-id="4e832-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4e832-114">-AppServicePlan</span></span>
<span data-ttu-id="4e832-115">App Service 方案物件</span><span class="sxs-lookup"><span data-stu-id="4e832-115">App Service Plan object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e832-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e832-116">-DefaultProfile</span></span>
<span data-ttu-id="4e832-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e832-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e832-118">-位置</span><span class="sxs-lookup"><span data-stu-id="4e832-118">-Location</span></span>
<span data-ttu-id="4e832-119">位於</span><span class="sxs-lookup"><span data-stu-id="4e832-119">Location</span></span>

```yaml
Type: String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e832-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e832-120">-Name</span></span>
<span data-ttu-id="4e832-121">WebApp 名稱</span><span class="sxs-lookup"><span data-stu-id="4e832-121">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e832-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e832-122">-ResourceGroupName</span></span>
<span data-ttu-id="4e832-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="4e832-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e832-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e832-124">CommonParameters</span></span>
<span data-ttu-id="4e832-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e832-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e832-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4e832-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e832-127">輸入</span><span class="sxs-lookup"><span data-stu-id="4e832-127">INPUTS</span></span>

### <span data-ttu-id="4e832-128">System.object</span><span class="sxs-lookup"><span data-stu-id="4e832-128">System.String</span></span>

## <span data-ttu-id="4e832-129">輸出</span><span class="sxs-lookup"><span data-stu-id="4e832-129">OUTPUTS</span></span>

### <span data-ttu-id="4e832-130">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="4e832-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="4e832-131">筆記</span><span class="sxs-lookup"><span data-stu-id="4e832-131">NOTES</span></span>

## <span data-ttu-id="4e832-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e832-132">RELATED LINKS</span></span>

[<span data-ttu-id="4e832-133">新-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4e832-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="4e832-134">移除-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4e832-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="4e832-135">重新開機-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4e832-135">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="4e832-136">開始-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4e832-136">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="4e832-137">停止 AzWebApp</span><span class="sxs-lookup"><span data-stu-id="4e832-137">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


