---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: c2780b05e6caae6e200e7fbab26f02a6644f9ebc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445899"
---
# <span data-ttu-id="6d609-101">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="6d609-101">Get-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="6d609-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6d609-102">SYNOPSIS</span></span>
<span data-ttu-id="6d609-103">取得 Azure Web App 憑證 SSL 系結。</span><span class="sxs-lookup"><span data-stu-id="6d609-103">Gets an Azure Web App certificate SSL binding.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d609-104">句法</span><span class="sxs-lookup"><span data-stu-id="6d609-104">SYNTAX</span></span>

### <span data-ttu-id="6d609-105">S1</span><span class="sxs-lookup"><span data-stu-id="6d609-105">S1</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d609-106">S2</span><span class="sxs-lookup"><span data-stu-id="6d609-106">S2</span></span>
```
Get-AzureRmWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d609-107">說明</span><span class="sxs-lookup"><span data-stu-id="6d609-107">DESCRIPTION</span></span>
<span data-ttu-id="6d609-108">**AzureRmWebAppSSLBinding** Cmdlet 會針對 Azure Web APP (SSL) 系結，取得安全通訊端層。</span><span class="sxs-lookup"><span data-stu-id="6d609-108">The **Get-AzureRmWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="6d609-109">SSL 系結是用來將 Web 應用程式與上傳的憑證建立關聯。</span><span class="sxs-lookup"><span data-stu-id="6d609-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="6d609-110">Web 應用程式可以系結至多個憑證。</span><span class="sxs-lookup"><span data-stu-id="6d609-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="6d609-111">示例</span><span class="sxs-lookup"><span data-stu-id="6d609-111">EXAMPLES</span></span>

### <span data-ttu-id="6d609-112">範例1：取得 Web 應用程式的 SSL 系結</span><span class="sxs-lookup"><span data-stu-id="6d609-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="6d609-113">這個命令會檢索與資源群組 ContosoResourceGroup 相關聯的 Web App ContosoWebApp SSL 系結。</span><span class="sxs-lookup"><span data-stu-id="6d609-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="6d609-114">範例2：使用物件參考來取得 Web 應用程式的 SSL 系結</span><span class="sxs-lookup"><span data-stu-id="6d609-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Get-AzureRmWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="6d609-115">這個範例中的命令也會取得 Web 應用程式 ContosoWebApp 的 SSL 系結;但在此情況下，會使用物件參照，而不是使用 Web App 名稱和相關聯的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d609-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="6d609-116">這個物件參照是由範例中的第一個命令所建立，它使用 **AzureRmWebApp** 來建立名為 ContosoWebApp 的 Web App 的物件參考。</span><span class="sxs-lookup"><span data-stu-id="6d609-116">This object reference is created by the first command in the example, which uses **Get-AzureRmWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="6d609-117">該物件參照會儲存在名為 $WebApp 的變數中。</span><span class="sxs-lookup"><span data-stu-id="6d609-117">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="6d609-118">這個變數及 **AzureRmWebAppSSLBinding** Cmdlet 接著是由第二個命令用來取得 SSL 系結。</span><span class="sxs-lookup"><span data-stu-id="6d609-118">This variable, and the **Get-AzureRmWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="6d609-119">參數</span><span class="sxs-lookup"><span data-stu-id="6d609-119">PARAMETERS</span></span>

### <span data-ttu-id="6d609-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d609-120">-DefaultProfile</span></span>
<span data-ttu-id="6d609-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6d609-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d609-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="6d609-122">-Name</span></span>
<span data-ttu-id="6d609-123">指定 SSL 系結的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d609-123">Specifies the name of the SSL binding.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d609-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d609-124">-ResourceGroupName</span></span>
<span data-ttu-id="6d609-125">指定指派憑證的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d609-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="6d609-126">您無法在同一命令中使用 *ResourceGroupName* 參數和 *WebApp* 參數。</span><span class="sxs-lookup"><span data-stu-id="6d609-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d609-127">-槽</span><span class="sxs-lookup"><span data-stu-id="6d609-127">-Slot</span></span>
<span data-ttu-id="6d609-128">指定 Web 應用程式部署槽。</span><span class="sxs-lookup"><span data-stu-id="6d609-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="6d609-129">若要取得部署槽，請使用 Get-AzureRMWebAppSlot Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6d609-129">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d609-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6d609-130">-WebApp</span></span>
<span data-ttu-id="6d609-131">指定 Web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="6d609-131">Specifies a Web App.</span></span>
<span data-ttu-id="6d609-132">若要取得 Web 應用程式，請使用 Get-AzureRmWebApp Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6d609-132">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d609-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="6d609-133">-WebAppName</span></span>
<span data-ttu-id="6d609-134">指定此 Cmdlet 取得 SSL 系結的 Web App 名稱。</span><span class="sxs-lookup"><span data-stu-id="6d609-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>

<span data-ttu-id="6d609-135">您無法在同一命令中使用 *WebAppName* 參數和 *WebApp* 參數。</span><span class="sxs-lookup"><span data-stu-id="6d609-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d609-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d609-136">CommonParameters</span></span>
<span data-ttu-id="6d609-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6d609-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d609-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6d609-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d609-139">輸入</span><span class="sxs-lookup"><span data-stu-id="6d609-139">INPUTS</span></span>

### <span data-ttu-id="6d609-140">網站地圖</span><span class="sxs-lookup"><span data-stu-id="6d609-140">Site</span></span>
<span data-ttu-id="6d609-141">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="6d609-141">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="6d609-142">輸出</span><span class="sxs-lookup"><span data-stu-id="6d609-142">OUTPUTS</span></span>

## <span data-ttu-id="6d609-143">筆記</span><span class="sxs-lookup"><span data-stu-id="6d609-143">NOTES</span></span>

## <span data-ttu-id="6d609-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d609-144">RELATED LINKS</span></span>

[<span data-ttu-id="6d609-145">新-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="6d609-145">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="6d609-146">移除-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="6d609-146">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="6d609-147">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="6d609-147">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


