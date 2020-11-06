---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCallbackUrl.md
ms.openlocfilehash: 56e1ebdddd25b424a4fb59f2065831d2b54f21b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452216"
---
# <span data-ttu-id="87e64-101">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="87e64-101">Get-AzureRmIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="87e64-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87e64-102">SYNOPSIS</span></span>
<span data-ttu-id="87e64-103">取得整合帳戶回撥 URL。</span><span class="sxs-lookup"><span data-stu-id="87e64-103">Gets an integration account callback URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87e64-104">句法</span><span class="sxs-lookup"><span data-stu-id="87e64-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87e64-105">說明</span><span class="sxs-lookup"><span data-stu-id="87e64-105">DESCRIPTION</span></span>
<span data-ttu-id="87e64-106">**AzureRmIntegrationAccountCallbackUrl** Cmdlet 會從資源群組取得整合帳戶回撥 URL。</span><span class="sxs-lookup"><span data-stu-id="87e64-106">The **Get-AzureRmIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="87e64-107">這個 Cmdlet 會傳回代表整合帳戶回撥 URL 的 **CallbackUrl** 物件。</span><span class="sxs-lookup"><span data-stu-id="87e64-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="87e64-108">指定整合帳戶名稱和資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="87e64-108">Specify the integration account name and resource group name.</span></span>

<span data-ttu-id="87e64-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="87e64-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="87e64-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="87e64-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="87e64-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="87e64-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="87e64-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="87e64-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="87e64-113">示例</span><span class="sxs-lookup"><span data-stu-id="87e64-113">EXAMPLES</span></span>

### <span data-ttu-id="87e64-114">範例1：取得整合帳戶回撥 URL</span><span class="sxs-lookup"><span data-stu-id="87e64-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="87e64-115">這個命令會取得整合帳戶回撥 URL。</span><span class="sxs-lookup"><span data-stu-id="87e64-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="87e64-116">參數</span><span class="sxs-lookup"><span data-stu-id="87e64-116">PARAMETERS</span></span>

### <span data-ttu-id="87e64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87e64-117">-DefaultProfile</span></span>
<span data-ttu-id="87e64-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="87e64-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="87e64-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="87e64-119">-Name</span></span>
<span data-ttu-id="87e64-120">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="87e64-120">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87e64-121">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="87e64-121">-NotAfter</span></span>
<span data-ttu-id="87e64-122">指定回撥 URL 的到期日。</span><span class="sxs-lookup"><span data-stu-id="87e64-122">Specifies the expiry date for the callback URL.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87e64-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87e64-123">-ResourceGroupName</span></span>
<span data-ttu-id="87e64-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="87e64-124">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87e64-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87e64-125">CommonParameters</span></span>
<span data-ttu-id="87e64-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87e64-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87e64-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="87e64-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87e64-128">輸入</span><span class="sxs-lookup"><span data-stu-id="87e64-128">INPUTS</span></span>

### <span data-ttu-id="87e64-129">所有</span><span class="sxs-lookup"><span data-stu-id="87e64-129">None</span></span>
<span data-ttu-id="87e64-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="87e64-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="87e64-131">輸出</span><span class="sxs-lookup"><span data-stu-id="87e64-131">OUTPUTS</span></span>

### <span data-ttu-id="87e64-132">CallbackUrl 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="87e64-132">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="87e64-133">筆記</span><span class="sxs-lookup"><span data-stu-id="87e64-133">NOTES</span></span>

## <span data-ttu-id="87e64-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="87e64-134">RELATED LINKS</span></span>

[<span data-ttu-id="87e64-135">AzureRmLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="87e64-135">Get-AzureRmLogicAppTriggerCallbackUrl</span></span>](./Get-AzureRmLogicAppTriggerCallbackUrl.md)


