---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
ms.openlocfilehash: c23e8ca566db3a3b3c93dcdc7a4fc53fc85979c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904078"
---
# <span data-ttu-id="78a26-101">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="78a26-101">Get-AzIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="78a26-102">簡介</span><span class="sxs-lookup"><span data-stu-id="78a26-102">SYNOPSIS</span></span>
<span data-ttu-id="78a26-103">獲得整合帳戶的 url。</span><span class="sxs-lookup"><span data-stu-id="78a26-103">Gets an integration account callback URL.</span></span>

## <span data-ttu-id="78a26-104">語法</span><span class="sxs-lookup"><span data-stu-id="78a26-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78a26-105">描述</span><span class="sxs-lookup"><span data-stu-id="78a26-105">DESCRIPTION</span></span>
<span data-ttu-id="78a26-106">**Get-Az有AccountCallbackUrl** Cmdlet 會從資源群組取得整合帳戶的 url。</span><span class="sxs-lookup"><span data-stu-id="78a26-106">The **Get-AzIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="78a26-107">此 Cmdlet 會傳回代表整合帳戶轉場 URL 的 **一個Url** 物件。</span><span class="sxs-lookup"><span data-stu-id="78a26-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="78a26-108">指定整合帳戶名稱和資源組名。</span><span class="sxs-lookup"><span data-stu-id="78a26-108">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="78a26-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="78a26-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="78a26-110">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="78a26-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="78a26-111">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="78a26-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="78a26-112">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="78a26-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="78a26-113">例子</span><span class="sxs-lookup"><span data-stu-id="78a26-113">EXAMPLES</span></span>

### <span data-ttu-id="78a26-114">範例 1：取得整合帳戶的 url</span><span class="sxs-lookup"><span data-stu-id="78a26-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="78a26-115">此命令會獲得整合帳戶的 url。</span><span class="sxs-lookup"><span data-stu-id="78a26-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="78a26-116">參數</span><span class="sxs-lookup"><span data-stu-id="78a26-116">PARAMETERS</span></span>

### <span data-ttu-id="78a26-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78a26-117">-DefaultProfile</span></span>
<span data-ttu-id="78a26-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="78a26-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78a26-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="78a26-119">-Name</span></span>
<span data-ttu-id="78a26-120">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="78a26-120">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78a26-121">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="78a26-121">-NotAfter</span></span>
<span data-ttu-id="78a26-122">指定付款 URL 的到期日。</span><span class="sxs-lookup"><span data-stu-id="78a26-122">Specifies the expiry date for the callback URL.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a26-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78a26-123">-ResourceGroupName</span></span>
<span data-ttu-id="78a26-124">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="78a26-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78a26-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a26-125">CommonParameters</span></span>
<span data-ttu-id="78a26-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="78a26-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a26-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="78a26-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a26-128">輸入</span><span class="sxs-lookup"><span data-stu-id="78a26-128">INPUTS</span></span>

### <span data-ttu-id="78a26-129">System.String</span><span class="sxs-lookup"><span data-stu-id="78a26-129">System.String</span></span>

## <span data-ttu-id="78a26-130">輸出</span><span class="sxs-lookup"><span data-stu-id="78a26-130">OUTPUTS</span></span>

### <span data-ttu-id="78a26-131">Microsoft.Azure.management.Logic.models.UvUrl</span><span class="sxs-lookup"><span data-stu-id="78a26-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="78a26-132">筆記</span><span class="sxs-lookup"><span data-stu-id="78a26-132">NOTES</span></span>

## <span data-ttu-id="78a26-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="78a26-133">RELATED LINKS</span></span>

[<span data-ttu-id="78a26-134">Get-AzLogicAppTriallcallbackUrl</span><span class="sxs-lookup"><span data-stu-id="78a26-134">Get-AzLogicAppTriggerCallbackUrl</span></span>](./Get-AzLogicAppTriggerCallbackUrl.md)


