---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 70C96DFC-F265-4792-AE62-DD224A4EE237
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 46cc7c75075cffface03af2ed70b5339dd36b0a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127782"
---
# <span data-ttu-id="8d082-101">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="8d082-101">Get-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="8d082-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d082-102">SYNOPSIS</span></span>
<span data-ttu-id="8d082-103">取得整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="8d082-103">Gets an integration account agreement.</span></span>

## <span data-ttu-id="8d082-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d082-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountAgreement [-ResourceGroupName <String>] [-Name <String>] [-AgreementName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d082-105">說明</span><span class="sxs-lookup"><span data-stu-id="8d082-105">DESCRIPTION</span></span>
<span data-ttu-id="8d082-106">**AzIntegrationAccountAgreement** Cmdlet 會從 Azure 資源群組取得整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="8d082-106">The **Get-AzIntegrationAccountAgreement** cmdlet gets an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="8d082-107">指定整合帳戶名稱、資源群組名稱和協定名稱。</span><span class="sxs-lookup"><span data-stu-id="8d082-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="8d082-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="8d082-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8d082-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="8d082-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8d082-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="8d082-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8d082-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="8d082-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8d082-112">示例</span><span class="sxs-lookup"><span data-stu-id="8d082-112">EXAMPLES</span></span>

### <span data-ttu-id="8d082-113">範例1：取得整合帳戶協定</span><span class="sxs-lookup"><span data-stu-id="8d082-113">Example 1: Get an integration account agreement</span></span>
```
PS C:\>Get-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/agreements/IntegrationAccount31
Name                   : IntegrationAccount31
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/24/2016 9:08:46 PM
ChangedTime            : 3/24/2016 9:08:59 PM
AgreementType          : AS2
HostPartner            : TestHost
GuestPartner           : TestGuest
HostIdentityQualifier  : XX
HostIdentityValue      : BB
GuestIdentityQualifier : ZZ
GuestIdentityValue     : AA
Content                : {"AS2":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ
                         ","Value":"ZZ"},"ProtocolSettings":{"MessageConnectionSettings":{"IgnoreCertificateNameMismatch":true,"SupportHttpStatusCodeCont
                         . . .
```

<span data-ttu-id="8d082-114">這個命令會取得名為 IntegrationAccountAgreement06 的整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="8d082-114">This command gets an integration account agreement named IntegrationAccountAgreement06.</span></span>

### <span data-ttu-id="8d082-115">範例2：依資源群組名稱取得整合帳戶協定</span><span class="sxs-lookup"><span data-stu-id="8d082-115">Example 2: Get integration account agreements by resource group name</span></span>
```
PS C:\>Get-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/agreements/IntegrationAccount31
Name                   : IntegrationAccount31
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/24/2016 9:08:46 PM
ChangedTime            : 3/24/2016 9:08:59 PM
AgreementType          : AS2
HostPartner            : TestHost
GuestPartner           : TestGuest
HostIdentityQualifier  : XX
HostIdentityValue      : BB
GuestIdentityQualifier : ZZ
GuestIdentityValue     : AA
Content                : {"AS2":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ
                         ","Value":"ZZ"},"ProtocolSettings":{"MessageConnectionSettings":{"IgnoreCertificateNameMismatch":true,"SupportHttpStatusCodeCont
                         . . .
```

<span data-ttu-id="8d082-116">這個命令會透過資源群組名稱取得整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="8d082-116">This command gets the integration account agreements by resource group name.</span></span>

## <span data-ttu-id="8d082-117">參數</span><span class="sxs-lookup"><span data-stu-id="8d082-117">PARAMETERS</span></span>

### <span data-ttu-id="8d082-118">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="8d082-118">-AgreementName</span></span>
<span data-ttu-id="8d082-119">指定整合帳戶協定的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d082-119">Specifies the name of an integration account agreement.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d082-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d082-120">-DefaultProfile</span></span>
<span data-ttu-id="8d082-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8d082-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d082-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="8d082-122">-Name</span></span>
<span data-ttu-id="8d082-123">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d082-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d082-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d082-124">-ResourceGroupName</span></span>
<span data-ttu-id="8d082-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d082-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d082-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d082-126">CommonParameters</span></span>
<span data-ttu-id="8d082-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d082-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d082-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8d082-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d082-129">輸入</span><span class="sxs-lookup"><span data-stu-id="8d082-129">INPUTS</span></span>

### <span data-ttu-id="8d082-130">System.object</span><span class="sxs-lookup"><span data-stu-id="8d082-130">System.String</span></span>

## <span data-ttu-id="8d082-131">輸出</span><span class="sxs-lookup"><span data-stu-id="8d082-131">OUTPUTS</span></span>

### <span data-ttu-id="8d082-132">IntegrationAccountAgreement 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="8d082-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="8d082-133">筆記</span><span class="sxs-lookup"><span data-stu-id="8d082-133">NOTES</span></span>

## <span data-ttu-id="8d082-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d082-134">RELATED LINKS</span></span>

[<span data-ttu-id="8d082-135">新-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="8d082-135">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="8d082-136">移除-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="8d082-136">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="8d082-137">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="8d082-137">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


